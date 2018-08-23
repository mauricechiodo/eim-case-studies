---
Title: The Equation
Template: LeafPage
---

# The Black-Scholes Equation

> $$ \frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} + rS \frac{\partial V}{\partial S} - rV = 0 ~, $$
> where
> $V = V(S,t)$ is the price of the option as a function of the stock price $S$ and time $t$,  
> $r$ is the risk-free interest rate, and $\sigma$ is the volatility of the stock.

## Derivation:

The underlying assumption to Black and Scholes' work is that the underlying stock price $S$ follos a geometric Brownian motion with drift $\mu$ and variance parameter $\sigma^2$:

 - *Brownian motion with drift:* A stochastic process $\lbrace X(t), t \geqslant 0 \rbrace$ is said to be a Brownian motion process with drift coefficient $\mu$ and variance paramter $\sigma^2$ if  
 (i) $\~\~$ $X(0) = 0$;  
 (ii) $\~\~$ $\lbrace X(t), t \geqslant 0 \rbrace$ has stationary and independent increments, in that the distribution of $X(t+s) - X(t)$ does not depend on $t$, and for all $t\_1 < t\_2 < ... < t\_n$, $X(t\_n) - X(t\_{n-1})$, $X(t\_{n-1}) - X(t\_{n-2}), ..., X(t\_2) - X(t\_1)$, and $X(t\_1)$ are independent;  
 (iii) $\~\~$ for every $t > 0$, $X(t)$ is normally distributed with mean $\mu t$ and variance $\sigma^2 t$.
