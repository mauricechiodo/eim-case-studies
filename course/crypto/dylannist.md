---
Title: Information on NIST
Template: LeafPage
---

$\newcommand{\lsb}[1]{\text{lsb}\_{240}\left( #1 \right)}$

# Background on NIST
The National Institute of Standards and Technology is a U.S. government organisation that aims to "to promote U.S. innovation and industrial competitiveness by advancing measurement science, standards, and technology in ways that enhance economic security and improve our quality of life." They have published a large variety of technical documents for technologies impacting on American government and society.

Notably, NIST have published a number of recommendations for cryptographic techniques, including methods for encryption, digital signatures, and secure random number generation. In 2006 NIST published *SP 800-90, Recommendation for Random Number Generation Using Deterministic Random Bit Generators* which included specifications for four different *cryptographic random number generators*. Among them was the *Dual Elliptic Curve Deterministic Random Bit Generator (Dual_EC_DRBG)*, an algorithm provided to NIST by the NSA, which fell under heavy criticism due to two large flaws. Secure RNGs are important in a lot of cryptographic applications, which rely on the assumption that an adversary cannot infer future output from the number generator given the previous sequence of values.

One of the two flaws found in the Dual EC DRBG was due to bias in the algorithm, which meant the numbers outputted by the generator were not distributed uniformly over the relevant range. 

The other flaw revolves around parameters used in the algorithm. These are provided by NIST without any justification as to how they were selected and it has been shown that they could have been generated in a specific way so as to enable a *kleptographic backdoor* which allows the original provider to execute an attack on instances of the DRBG without other parties being able to do the same. That is to say, given some knowledge about relations between the DRBG's parameters, there exists an efficient algorithm to infer the internal state of the random number generator and predict the future output.

# The Dual_EC_DRBG (2006) Algorithm
(ref Barker and Kelsey)

The specification for the Dual_EC_DRBG provides three elliptic curves which the algorithm can be run over. The recommended curve is described below and is chosen so that both the field and the elliptic curve defined over it are cyclic and of prime order.

Let $p = 2^{256} - 2^{224} + 2^{192} + 2^{96} - 1$.

${E(\mathbb{F_p})}$ denotes the elliptic curve over ${\mathbb{F}_p}$ defined by 
$$ y^2 = x^3 - 3x + b $$
and
$$ b = 41058363725152142129326129780047268409114441015993725554835256314039467401291. $$

Let $P = (x_P, y_P), Q = (x_Q, y_Q)$ where
$$ x_P = 48439561293906451759052585252797914202762949526041747995844080717082404635286, $$
$$ y_P = 36134250956749795798585127919587881956611106672985015071877198253568414405109, $$
$$ x_Q = 91120319633256209954638481795610364441930342474826146651283703640232629993874, $$
$$ y_Q = 80764272623998874743522585409326200078679332703816718187804498579075161456710. $$

($a, b, x_P, y_P, x_Q, y_Q$ ref Barker and Kelsey 2005)

A seed ${s_0}$ is chosen randomly from $\\{0, 1, ..., |E(\mathbb{F}_p)|-1\\}$. 

Let ${x: E(\mathbb{F}_p) \rightarrow \mathbb{F}_p}$ be the function projecting points onto their ${x}$-coordinate. $\mathrm{lsb}_i(s)$ denotes the ${i}$ least significant bits of an integer ${s}$.

The Dual_EC_DRBG algorithm maps the seed to a pseudorandom sequence of length $240k$ as so:

- for $i=1...k$:
  - let $s\_i = \lsb{x(s\_{i-1}P)}$
  - let $r\_i = \lsb{x(s\_iQ)}$
- return $(r_1, ..., r_k)$

The claim is that due to the difficulty of solving the discrete logarithm (finding an integer $\alpha$ such that $P = \alpha Q$) it is intractable to work backwards to find the internal state $s_i$ of the number generator.

# Output Bias
(ref Schoenmakers and Sidorenko) has a nice presentation of the issue – indeed, I believe that it was the original paper drawing attention to the presence of this bias.

I'm not sure if this is overly relevant in this case, however. It seems probable that it is a genuine mistake, and it is not clear whether it could be practically exploited. However, it may provide a method by which one could identify that the Dual_EC_DRBG is being used over some other RNG. Additionally, they did make the decision not to fix the flaw even after it had attracted a lot of attention, for the reasons that "some internal discussion in X9 that said this was just a theoretical issue" and "it was the NSA’s algorithm, we largely let them respond to comments on it". 

# The Possibility of a Backdoor
There is no public knowledge as to how ${P}$ and ${Q}$ were generated. It is known that ${P}$ should be chosen to be a generator of the group, but in our case this is true of all elements. (ref Bernstein et al) explains that, even after inquiring as to the origin of ${P}$ and ${Q}$, John Kelsey (one of the two authors in the NIST paper) was told that the NSA had "generated $(P, Q)$ in a secure, classified way" and had "kyboshed" the idea of generating ${Q}$ in a transparent way. The security of the algorithm however depends on the difficulty of solving the ECDLP, $Q = \alpha P$, but there is no reason the NSA couldn't have generated ${Q}$ by first choosing some arbitrary ${\alpha}$, removing the need to solve the discrete logarithm altogether. 

If such an $\alpha$ is known, then we can attempt to infer the internal state of the RNG as so:

- Given some $r\_i = \lsb{x(s\_iQ)}$, we can enumerate the $2^16$ integers, $x_j$ whose first 240 bits match $r_i$.

- We build a set ${S}$ of candidate points on the RNG.

- For each $x_j$:

  - Compute $z_j = (r_i^j)^3 - 3r_i^j + b$
  
  - If $z_j$ is a quadratic residue modulo ${p}$ (ie if some number squares to it) then we can add to ${S}$ $(y_1, x_j)$ and $(y_2, x_j)$, where $y_1^2 \equiv y_2^2 \equiv z_j \pmod{p}$.
  
- We should now have that $s_iQ \in S$ although we do not know which element of ${S}$ this is.

- Now note that contained in $\alpha\cdot S$ we have

$$ \begin{aligned} \alpha (s_i Q) 
&= (\alpha s_i) Q \\\\
&= (s_i \alpha) Q \\\\
&= s_i (\alpha Q) \\\\
&= s_i P
\end{aligned} $$.

- And $s\_{i+1} = \lsb{x(s\_i)}.$

By looking at multiple sequential outputs from the RNG we can quickly reduce our set of candidate states to a small number of possibilities, compromising its integrity.

The specification paper also documents how one can generate their own values for ${P}$ and ${Q}$, but does not explain why one would want to do so, and further requires someone to use the NSA's values if they want FIPS security verification. 

# NIST's Response

In 2015 NIST updated their recommendation paper for cryptographic random number generators, removing the Dual_EC_DRBG from the paper entirely. They conducted an internal review from 2013-2016 looking at why the EC_DRBG was allowed to remain in their recommendations for so long. The authors of the original specification have conceded in presentations that "Dual EC DRBG should not have been included in X9.82 or SP 800-90 in current form" and it has emerged that the issues that have been raised over the algorithm were discussed internally prior to their discovery by the public. The main reasons given for why the standard we ahead were that

- "Dual EC DRBG is extremely slow, and seemed unlikely to see much use; so putting a trapdoor in seemed kind-of pointless."
  - However, it did eventually see a fair amount of use in some places.
  
- "NSA claimed to have existing customers who were using the DRBG, and wanted to be able to get FIPS validation."

- "We didn’t believe a backdoor in this algorithm was likely."
  - But evaluating security based on speculation seems foolish at best.
  - Kelsey has stated that they "should have asked: Should we include an algorithm in our standards that could have a trapdoor?" rather than "do we think there is a trapdoor into Dual EC DRBG?"

Despite providing documentation on the method for selecting new ${P}$ and ${Q}$ for the algorithm, the group conducting the review were unable to find evidence that anyone had made use of this option "not even organizations with a lot of cryptographic expertise."

# Aftermath
The suspicion around the Dual EC DRBG casts some doubt over the trustworthiness of NIST's other proceedings. Although the relevant individuals claimed to also be unaware as to the origins of the parameters in the algorithm and whether or not there does exist a back door, the willingness of some of these individuals to blindly follow orders from the NSA is alarming. Despite some people attempting to raise issues with the flaws in their work, it took nearly 10 years (and a large scale leak of NSA documents, some heavily suggesting a backdoored technology in NIST's repertory, followed by public outrage) before the recommendation was withdrawn. This specific algorithm had a very obvious flaw and it could be spotted by the public, but NIST has published a large collection of other cryptographic algorithms and technologies, any of which could have more subtle vulnerabilities which have also been kept quiet by ties to the NSA.
