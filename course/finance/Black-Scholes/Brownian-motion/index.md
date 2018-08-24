---
Template: LeafPage
---

#Brownian motion
 
---

 - *Standard Brownian motion:* A stochastic process $\lbrace X(t), ~ t \geqslant 0 \rbrace$ is said to be a standard Brownian motion process if  
 (i) $X(0) = 0$ ;  
 (ii) $\lbrace X(t), ~ t \geqslant 0 \rbrace$ has stationary and independent increments, in that the distribution of $X(s+t) - X(t)$ does not depend on $t$, and for all $t\_1 < t\_2 < ... < t\_n$, the increments $X(t\_n) - X(t\_{n-1})$, $X(t\_{n-1}) - X(t\_{n-2})$, ..., $X(t\_2) - X(t\_1)$, $X(t\_1)$ are independent;  
 (iii) for every $t > 0$, $X(t)$ is normally distributed with mean $0$ and variance $t$.
 
---

 - *Brownian motion with drift:* We say that $\lbrace X(t), ~ t \geqslant 0 \rbrace$ is a Brownian motion process with drift coefficient $\mu$ and variance paramter $\sigma^2$ if  
 (i) $X(0) = 0$ ;  
 (ii) $\lbrace X(t), ~ t \geqslant 0 \rbrace$ has stationary and independent increments;  
 (iii) for every $t > 0$, $X(t)$ is normally distributed with mean $\mu t$ and variance $\sigma^2 t$.

An equaivalent definition is to let $\lbrace B(t), ~ t \geqslant 0 \rbrace$ be standard Brownian motion and then define $X(t) = \sigma B(t) + \mu t$.

---

 - *Geometric Brownian motion:* If $\lbrace Y(t), ~ t \geqslant 0 \rbrace$ is a Brownian motion process (possibly with non-standard drift and variance parameter), then the process $\lbrace X(t), ~ t \geqslant 0 \rbrace$ defined by $X(t) = e^{Y(t)}$ is called geometric Brownian motion.

---
