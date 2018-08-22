---
Title: Elliptic Curve Cryptography
Template: ListSubPages
---

# Elliptic Curve Cryptography

Elliptic Curve Cryptography is a set of algorithms for encrypting and decrypting data through
exchange of a public key. Public-key cryptography works on the idea of a trapdoor function
which is easy to compute in one direction, but hard to compute in the opposite direction. Two
popular methods, Diffie-Hellman and RSA, work with the trapdoor function of factorising large
prime numbers [12]. However these methods have encountered drawbacks such developments in
improved prime factorisation algorithms such as the general number field sieve [14] and repeated
use of the same primes, meaning that it was feasible for the number field sieve algorithm to be
applied. Elliptic curves provide a much stronger alternative trapdoor function.
Points on the curve satisfy an equation of the form:
$$y^2=x^3+ax+b.$$

The basic idea behind elliptic curve cryptography is that if we add a point together with itself in the sense shown in the diagram $n$ times then given the values of $P_0$ and $P_n$, $n$ is very difficult to determine.

![Elliptic Curve](http://db716.user.srcf.net/eim/media/curve1.png)

In reality, elliptic curve cryptography doesn't use a curve in the form as shown in the figure. For
use in cryptography, we take the curve over $\mathbb{F}_q$ (finite field with q elements) and only consider
rational points, over $\mathbb{F}_q$ this amounts to a finite number of points. We can formalise the addition
as illustrated in the figure.

Let $P=(x_p,y_p), Q=(x_q,y_q)$ and $R=(x_r,y_r)$. Then given $P$ and $Q$, 
$$x_r=\lambda^2-x_p-x_q$$ 
$$y_r=\lambda(x_p-x_r)-y_p$$
where
$$\lambda = \frac{y_q-y_p}{x_q-x_p}.$$

Using this as the group addition operation, we have made a finite additive group using the elliptic curve, call it $E(\mathbb{F}_q)$. 

Using elliptic curves in cryptography relies on the discrete logarithm problem being difficult. The problem is the following: given a group G and elements $P$ and $Q$, find an integer k such that $kP = Q$ (given such a k exists). By choosing $q=p^n$ for a prime $p$ in our finite field, the discrete logarithm problem for our elliptic curve is found to be difficult, and hence a good trap door function. The discrete logarithm problem using the elliptic group $E(\mathbb{F}_q)$ is orders of magnitude harder than the corresponding cyclic group of order $p$ [cite].

![Graph](http://db716.user.srcf.net/eim/media/ellipticVsConv.jpg)

The consequence of the elliptic curve discrete logarithm being a harder problem to solve is that it allows a smaller key size to be used. This means that it is possible to use this kind of cryptography in constrained devices because the cryptographic operations are faster, run on smaller chips or on more compact software. Therefore there is less power consumption and less heat production [cite].

Consider an elliptic curve $E$ over $\mathbb{F}_q$ with group order $n=$#$E(\mathbb{F}_q)$. Here we will detail some attacks on the elliptic curve discrete logarithm problem:

- **Baby Step, Giant Step** [cite]: This is the fastest general method for solving the problem and can be applied to any curve. It runs in  $\sqrt{n}$ time and $\sqrt{n}$ space with $n$ defined above as #$E(\mathbb{F}_q)$, this is not fast enough to be feasible for the $n$ used in encryption. Recall that the discrete logarithm problem is to find $k$ such that $kP = Q$ for points $P$ and $Q$ on the elliptic curve. The algorithm is as follows:
  	- Pick and integer $m>\sqrt{n}$.
		- Compute $mP$.
		- For $i=0$ to $i=m-1$ compute and store $iP$.
		- For $j=0$ to $j=m-1$ compute and store $Q-jmP$
		- Sort the lists from the previous two steps in a consistent way.
		- Compare the lists until a pair $i,j$ such that $iP=Q-jmP$ is found.
		- Return $k\equiv i+jm \pmod{n}$.
	
- **MOV attack** [cite]: This attack can only be used on certain types of curves. It reduces the discrete logarithm problem on an elliptic curve $E(\mathbb{F}_q)$ 
to a discrete logarithm problem on 
$\mathbb{F}_{q^m}$ for some $m$. This attack is more complicated, but the cited paper includes the details of the attack if readers are interested. 


In order for the elliptic curve $E$ to make the discrete logarithm problem as hard as it can be, we require [cite]:
- The group should have a subgroup of large prime order $r$ which is of several hundred bits in length, as of 1999 160 bits was considered to be the minimum. This prevents the Pollard-$\rho$-attack (not discussed). 
- The curve should not be anomalous i.e $q=n=p$ a prime. This prevents a Semaev-Smart-Satoh-Araki attack (not discussed).
- To prevent a MOV attack, we need to ensure that the order of $P$ does not divide $q^k-1$ for all $k$ such that $1\leq k \leq C$, where $C$ is sufficiently large such that the discrete logarithm problem on $\mathbb{F}_{q^C}^{\times}$ is difficult to solve.  



One of the main approaches for finding a suitable curve is to generate random curves and compute their group orders until an appropriate one is found [cite]. If we pick a curve $E(\mathbb{F}_q):y^2=x^3+ax+b$ by randomly selecting $a,b \in \mathbb{F}_q$ such that $4a^3+27b^2 \neq 0$ if $q$ is odd and $b \neq 0$ if $q$ is a power of 2 then it turns out that a large fraction of the time, the above conditions are satisfied [cite]. 

There are a few ways that the elliptic curve can be used to encrypt. One method is to use a Diffie-Hellman method; instead of using the cyclic group corresponding to $\mathbb{F}_q$, we use our new elliptic curve group; the private key ($priv$) is the number of times we dot a public point with itself and the public key is the public point dotted with itself $priv$ times. To make the shared secret, Alice and Bob do the following [cite]:
- Alice and Bob agree on an elliptic curve E over a finite field $\mathbb{F}_q$, chosen so that the discrete logarithm problem is difficult, and a public point $P$ on the curve.
- Alice chooses a secret number $a$ and sends Bob $aP$ with the appropriate elliptic group multiplication, $E(\mathbb{F}_q$).
- Bob chooses a secret number $b$ and sends Alice $bP$ multiplication in the same way.
- They can then both calculate $(a+b)P$ which becomes their secret key. 


Another method is known as Massey-Omera Encryption, the concept is that if Alice wants to send Bob a message securely, Alice sends Bob a box with her lock on it, Bob adds his lock and sends the box back to Alice, who removes her lock and then sends the box back to Bob who can remove his lock and open the box [cite]:
- Once again, Alice and Bob agree on a curve $E(\mathbb{F}_q)$ chosen so that the discrete logarithm problem is hard. Let $n=$#$E(\mathbb{F}_q)$.
- Alice represents her message by $P \in E(\mathbb{F}_q)$.
- Alice choose a secret $a \in \mathbb{Z}$ such that gcd$(b,n)=1$, computes $aP$ and sends it to Bob. 
- Bob chooses a secret $b \in Z$ such that gcd$(b,n)=1$, computes $b(aP)=baP$, and sends it to Alice
- Alice find $a^{-1} \in \mathbb{Z}_n$, computes $a^{-1}(baP)=a^{-1}baP$, and sends it to Bob
- Bob finds $b^{-1} \in \mathbb{Z}_n$, computes $b^{-1}(a^{-1}baP)=b^{-1}a^{-1}baP$, and takes the result to be the message.

This is valid because $b^{-1}a^{-1}baP=P$. To show this, it is enough to show that $a^{-1}aR=R$ for $R \in E(\mathbb{F}_q)$ as the $a$'s and $b$'s commute and are symmetric. We chose $a$ such that gcd$(a,n)=1$, so we know that $a^{-1}$ exists and that $a^{-1}a \equiv 1$. Therefore $a^{-1}a = 1 +kn$ for some $k$. The group order is $n$ so $R$ has order which divides $n$, i.e $nR=\mathcal{O}$. Therefore $a^{-1}aR=(1+kn)R=R+k\mathcal{O}=R$ as required.






