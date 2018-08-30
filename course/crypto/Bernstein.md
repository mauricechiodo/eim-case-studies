---
Title: Bernstein
Template: ListSubPages
---

# Bernstein

While he was a graduate at the University of California, Daniel J. Bernstein developed an encryption algorithm called 'Snuffle,' a system which converts a one-way hash function into a zero-delay private-key encryption system [1]. He wanted to publish the algorithm, a paper explaining the algorithm and the source code allowing a computer to run the algorithm. He also wanted to discuss his work in an educational capacity at public events and to hear academic opinions on his technique. However, under the Arms Export Control Act and the International Traffic in Arms Regulations (which aimed to control the export of cryptography so that it wouldn't interfere with the government's efforts to analyse encrypted traffic [2]) the US government required him to submit his work for review, register as an arms dealer and apply for and obtain a license from the government to publish his ideas. The penalties for failing to do so would be a one million dollar criminal fine, ten years in jail, and civil fines [1]. Bernstein believed this violated the first amendment so sued the government with sponsorship from the EFF (Electronic Frontier Foundation). The court ruled in Bernstein's favour, saying that the software source code was speech protected by the First Amendment [3]. 


Bernstein has continued to work in cryptography. He has a blog [4] which includes insightful blog posts, including one entitled "NIST's cryptographic standardization process" which discusses NIST's questionable cryptographic standards. The blog post contains a letter that Bernstein wrote to NIST in lieu of a report they wrote entitled "NIST cryptographic standards and guidelines development process". Bernstein highlighting past failings on NIST's part, namely standardising cryptographically unsound security. He also berates NIST for continuing to claim that they "the most secure and trusted cryptographic standards" and that these standards provide "high-quality, cost-effective security mechanisms" when the cryptographic community has known this is not true for many years. Crucially, the draft doesn't propose mechanisms to prevent NIST from promoting insecure cryptographic standards in the future. Bernstein claims that the draft report is "very difficult to take seriously." It's important to note that Bernstein has received grants from NIST, but despite this, the letter/blog post is certainly not in favour of their behaviour.

Bernstein is co-author of a webpage giving advice on how to choose safe elliptic curves called 'SafeCurves' [5]. The SafeCurves web site reports security assessments of various specific curves and highlights that there are many attacks that break real-world elliptic curve cryptography without solving the discrete logarithm problem due to bad implementation. All of the NIST curves reviewed have been assessed as 'unsafe.'

In September 2017 Bernstein co-authored a review published in Nature entitled "Post-Quantum Cryptography" [6] which talks about cryptography under the assumption that an attacker has access to a large quantum computer, which would make the currently used encryption methods unsecure, including elliptic curve cryptography. Therefore, research into post-quantum cryptography is very important to ensure the durability of digital security. The review discusses the impact that quantum computers could have on common methods of encryption, such as the use of Shor's algorithm to break RSA and the impact of Grover's algorithm on many more cryptographic systems, and goes on to discuss more secure alternatives. 


The table from "Post-Quantum Cryptography" [6] illustrating the potential effect of quantum computers on the security of common encryption methods. Security levels shown are against the best pre-quantum and post-quantum attacks known. Security level $b$ means that the best attacks use approximately $2^b$ operations.

![TableBernstein](http://cueimps.soc.srcf.net/course/media/BernsteinGraph.png)
	
The article makes the important point that many applications of cryptography require all parties to use the same cryptographic system and therefore it's important that the process of standardisation comes well in advance of quantum computers. 

Regardless of whether quantum computers become a reality in the near future or not, there is no doubt that a lot of research and development is going into post-quantum cryptography (EU Horizon 2020 PQCRYPTO project, Google New Hope) because of the major implications quantum computers would have on our current encryption methods, rendering even the best elliptic curve cryptography unsafe.

# References
[1] [Jo-Anne Kokoski. Dan Bernstein's Attempt to Publish Snuffle and The Le-
gal Issues Raised, 1995.](http://groups.csail.mit.edu/mac/classes/6.805/student-papers/fall95-
papers/kokoski-crypto.html)

[2] [NIST-National Institute of Standards and Technology.](https://www.nist.gov/national-
institute-standards-and-technology)

[3] [Bernstein v. US Department of Justice, July 2011](https://www.eff.org/cases/bernstein-v-us-dept-justice)

[4] [Daniel Bernstein Blog](https://blog.cr.yp.to/)

[5] [Daniel Bernstein and Tanja Lange. SafeCurves: Introduction](https://safecurves.cr.yp.to/)

[6] [Daniel J. Bernstein and Tanja Lange. Post-quantum cryptography. *Nature*](https://www.nature.com/articles/nature23461)
