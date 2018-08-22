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




