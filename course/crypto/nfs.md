---
Title: Attacking Diffie-Hellman
Template: LeafPage
---

# The dangers of precomputation: an attack on Diffie-Hellman

The number field sieve algorithm (as detailed in Adrian et al., 2015) is a two-part process, with the first part having three stages: firstly, a field is selected by quotienting out $Q(z)/f(z)$ for some convenient polynomial $f(z)$, of degree around $6$; secondly, 'sieving' takes place, in which the elements of the field are separated into certain sections with the 'B-Smooth' property; thirdly, a sparse matrix is constructed to encode the prime factorisations calculated, which can be used to find the logs of small elements. Note that all this can be calculated only from the prime $p$.

The second part, the 'descent', calculates the log of a given input $y$ by relating it to the small logs already calculated; compared to the first part it is computationally fast, and so the overall method is computationally feasible for many inputs, since the precomputation on $p$ need only be done once.

The authors of that paper found that for the most common 512-bit prime used in the Apache group, a standard unoptimised number field sieve setup cracked the key in around a week of computation on about 2500 parallel CPU cores; after this was performed, each specific descent required just over a minute, thus providing a computationally feasible mechanism. They hypothesise that keys corresponding to 1024-bit primes could be broken on a 'nation-state level' of computational capacity, and indeed refers to material from media leaks to argue that the NSA has done just that.

It is interesting to note that Diffie himself recognised the possibility of this form of attack in a 1988 paper (presumably having realised it long before), though he largely dismissed it, given its apparently unmanageable runtime of order 

$$\exp{\sqrt{\log{p}\log{\log{p}}}}$$

for a given prime $p$. Of course, hardware developments in the intervening decades have shifted the goalposts rather drastically, and his scheme has an insecurity he could hardly have expected to have been practically exploited. This goes to show the importance of considering future technological developments when creating algorithms in this manner.

It is still by no means easy for the NSA to do this: each prime takes around six months to analyse, and in that regard they are very lucky that only a small number of primes, known as the 'Oakley group', are used for the vast, vast majority of encryption over the internet. It is difficult to generate so-called 'safe' primes (of the form $2p+1$, where $p$ is also prime), and every man and his dog knowing $p$ does not, on the face of it, affect security. However, this paucity of usable primes meant the NSA had a manageable task. And, thanks to Snowden, it seems clear that they took it up with some gusto.

I mean, on some level we know – we have always known – that this is happening. Given that it was possible, it has happened – the benefit for the government is too high, the costs too low, for it not to be the case. Yet it remains that on a major level, this wholesale decryption of internet traffic, this bludgeoning to a savage death of the very concept of privacy, has spattered blood upon the hands of guilty mathematicians. It is next to impossible to successfully code the number field sieve, let alone to improve it to a usable efficiency, without some knowledge of Galois theory and the mathematical maturity that presupposes. This is, quite utterly, quite obviously, a matter for the ethics of mathematics.

## Later developments

For the moment, the situation perhaps isn't quite critical, but it is well on the way to being so. Most firms still using 512-bit primes rolled out patches soon after the publication of the aformentioned paper, though some vulnerabilities no doubt remain; Halderman and Teague (2015) raised its potential impact on a 2015 state election in New South Wales, at the time the largest-scale instance of online voting.

However, mathematical developments have also been made – and, almost incredibly, mostly on the side of the NSA. For instance, a late 2015 paper by Guillevic showed how the individual computations of discrete logarithms – that is, after the precomputation has been carried out – could be rendered much more efficient, especially when working in fields of size $p^n$ where $n$ is small; this works by optimising the boot stage of this descent part.

But enough of the detail. Is it not absurd that, at a time when internet traffic is being preyed on more than ever before – by our government, by foreign powers, by malevolent forces beyond our ken – mathematicians are unthinkingly publishing papers which actively abet this? (Perhaps more concerningly, what if they *are* thinking about this?) 

There are not masses of these papers, to be sure. We are not in a position where if one mathematician does not publish it, another will – this is certainly an active choice on the researchers' parts. Yet there are enough of them that, combined, they could render attacks on security considerably more potent. It is one thing for research to, some years after the fact, produce adverse consequences; it is quite another for research to go on in full knowledge of such a context. In circumstances such as these, it is high time that mathematicians should start seriously considering the ethical impact of their work.
