---
Title: NIST
Template: ListSubPages
---

# NIST and Elliptic Curve Cryptography

The National Institute of Standards and Technology (NIST) is a US government organisation that aims to "to promote US innovation and industrial competitiveness by advancing measurement science, standards, and technology in ways that enhance economic security and improve our quality of life."

They are a physical laboratory who have published a large variety of technical documents, which include details on how people should use elliptic curve cryptography. This has sparked controversy because they have been found to support and standardise unsafe cryptography. We will start by discussing what elliptic curve cryptography is before going into some of the unsavoury things that NIST have done.


Elliptic curve cryptography is a set of algorithms for encrypting and decrypting data through exchange of a public key. Public-key cryptography works on the idea of a trapdoor function which is easy to compute in one direction, but hard to compute in the opposite direction. We have already discussed one example in our discussion of Diffie-Hellman which uses the trapdoor function of factorising large prime numbers. However, we have already seen that this method has encountered drawbacks such developments in improved prime factorisation algorithms such as the general number field sieve. RSA, another popular encryption method suffers from the same issue. Elliptic curves provide a much stronger alternative trapdoor function.

Points on an elliptic curve satisfy an equation of the form:
$$ \begin{equation}
y^2 = x^3 + ax + b
\end{equation}
 $$.
 
The basic idea behind elliptic curve cryptography is that if we add a point together with itself in the sense shown in the diagram $n$ times then given the values of $P_0$ and $P_n$, $n$ is very difficult to determine. 

![Elliptic Curve](http://db716.user.srcf.net/eim/media/curve1.png)

In the attached notes, we go into how elliptic curves are used in cryptography, but essentially we can make a finite group using the curve. Addition of points work in very much the same way as illustrated in the diagram. What makes this useful for cryptography is that finding $n$ from $P_0$ and $P_n$ requires solving the discrete logarithm problem for elliptic curves - it is a much more difficult problem than the the normal discrete logarithm we met when discussing Diffie-Hellman.

Certain elliptic curves make the discrete logarithm problem particularly difficult. These depend on the finite group that we can construct from the curve, so we save these details for the notes. The fact that certain curves are better than others means that many people rely on companies like NIST to provide them with safe curves...

(still to do: need to include a summary of Dylan's NIST work and combine our reports to make one detailed document and work out how to get the diagram to show on the website)
