---
Title: The Formula
Template: LeafPage
---

# The Black-Scholes Formula

After [deriving the Black-Scholes equation](2Equation),

$$ \frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} + rS \frac{\partial V}{\partial S} - rV = 0 ~, $$

we can go about attempting to solve it, so that we might price particular options. First, we simplify the form of the equation.  
Setting $V(S,t) = e^{-r(T-t)} y(S,t)$, the equation gives

$$ r e^{-r(T-t)} y + e^{-r(T-t)} \frac{\partial y}{\partial t} + \frac{1}{2} \sigma^2 S^2 e^{-r(T-t)} \frac{\partial^2 y}{\partial S^2} + rS e^{-r(T-t)} \frac{\partial y}{\partial S} - r e^{-r(T-t)} y = 0 ~, $$

or, after cancellations

$$ \frac{\partial y}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 y}{\partial S^2} + rS \frac{\partial y}{\partial S} = 0 ~. $$

Now we make a change of variables $y(S,t) = y(\xi,\eta)$, where

$$ \begin{aligned}
\xi &= \frac{2}{\sigma^2} \left( r - \frac{1}{2} \sigma^2 \right) \left( \log \left( \frac{S}{c} \right) + \left( r - \frac{1}{2} \sigma^2 \right) (T - t) \right) ~, \\\\
\eta &= \frac{2}{\sigma^2} \left( r - \frac{1}{2} \sigma^2 \right) (T - t) ~,
\end{aligned} $$

and $c$ is the strike price of our option. We have

$$ \begin{aligned}
\frac{\partial}{\partial t} &= - \frac{2}{\sigma^2} \left( r - \frac{1}{2} \sigma^2 \right)^2 \left( \frac{\partial}{\partial \xi} + \frac{\partial}{\partial \eta} \right) ~, \\\\
S \frac{\partial}{\partial S} &= \frac{2}{\sigma^2} \left( r - \frac{1}{2} \sigma^2 \right) \frac{\partial}{\partial \xi} ~.
\end{aligned} $$

With these, we can simplify the partial differential equation for $y(\xi, \eta)$ as follows:

$$ \begin{aligned}
0 &= \frac{\partial y}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 y}{\partial S^2} + rS \frac{\partial y}{\partial S} \\\\
&= \frac{\partial y}{\partial t} + \frac{1}{2} \sigma^2 \left( S \frac{partial}{\partial S} \left( S \frac{\partial y}{\partial S} \right) - S \frac{\partial y}{\partial S} + rS \frac{\partial y}{\partial S} \\\\
&= \frac{\partial y}{\partial t} + \frac{1}{2} \sigma^2 S \frac{partial}{\partial S} \left( S \frac{\partial y}{\partial S} \right) + \left( r - \frac{1}{2} \sigma^2 \right) S \frac{\partial y}{\partial S}
\end{aligned} $$
