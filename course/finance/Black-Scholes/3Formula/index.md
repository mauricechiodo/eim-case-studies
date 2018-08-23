---
Title: The Formula
Template: LeafPage
---

# The Black-Scholes Formula

After [deriving the Black-Scholes equation](2Equation),

$$ \frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} + rS \frac{\partial V}{\partial S} - rV = 0 ~, $$

we can go about attempting to solve it, so that we might price particular options. First, we simplify the form of the equation.  
Setting $V(S,t) = e^{-r(T-t)} y(S,t)$, where $T$ is the maturity date of our option, the equation gives

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
&= \frac{\partial y}{\partial t} + \frac{1}{2} \sigma^2 \left( S \frac{\partial}{\partial S} \left( S \frac{\partial y}{\partial S} \right) - S \frac{\partial y}{\partial S} \right) + rS \frac{\partial y}{\partial S} \\\\
&= \frac{\partial y}{\partial t} + \frac{1}{2} \sigma^2 S \frac{\partial}{\partial S} \left( S \frac{\partial y}{\partial S} \right) + \left( r - \frac{1}{2} \sigma^2 \right) S \frac{\partial y}{\partial S} \\\\
&= -\frac{2}{\sigma^2} \left( r - \frac{1}{2} \sigma^2 \right)^2 \left( \frac{\partial y}{\partial \xi} + \frac{\partial y}{\partial \eta} - \frac{\partial^2 y}{\partial \xi^2} - \frac{\partial y}{\partial \xi} \right) ~.
\end{aligned} $$

Thus, after cancellations:

$$ \frac{\partial y}{\partial \eta} - \frac{\partial^2 y}{\partial \xi^2} = 0 ~. $$

We can now identify this as a diffusion equation. In order to solve it we must consider what type of options in particular we are trying to price, so that we can establish boundary conditions:

To start with, suppose we have a European call option $V$, with strike price $c$ and which matures at time $T$. At maturity, this option has payout

$$ V(S,T) = \begin{cases}
S - c &  \text{if } S \geqslant c \\\\
0 & \text{if } S < c
\end{cases} ~, $$

(corresponding to whether the buyer should exercise the option or not).  
After the change of variables above, this becomes the initial condition

$$ y(\xi,0) = \begin{cases}
c \exp \left( \frac{\frac{1}{2} \sigma^2 \xi}{r - \frac{1}{2} \sigma^2} \right) - c &  \text{if } \xi \geqslant 0 \\\\
0 & \text{if } \xi < 0
\end{cases} ~. $$

Black and Scholes use the solution to this particular boundary value problem given by Churchill {reference}:

$$ \begin{aligned}
y(\xi,\eta) &= \frac{1}{\sqrt{\pi}} \int\_{-\infty}^{\infty} y(\xi + 2x \sqrt{\eta}, 0) e^{-x^2} dx \\\\
&= \frac{1}{\sqrt{2\pi}} \int\_{-\infty}^{\infty} y(\xi + q \sqrt{2\eta}, 0) e^{-\frac{1}{2} q^2} dq \\\\
&= \frac{c}{\sqrt{2\pi}} \int\_{- \xi / \sqrt{2\eta}}^{\infty} \left( \exp \left( \frac{1}{2} \sigma^2 \left( \xi + q\sqrt{2\eta} \right) \big/ \left( r - \frac{1}{2} \sigma^2 \right) \right) - 1 \right) e^{-\frac{1}{2} q^2} dq \\\\
&= \frac{c}{\sqrt{2\pi}} \int\_{- \xi / \sqrt{2\eta}}^{\infty} \exp \left( -\frac{1}{2} \left( q^2 - 2 \alpha q \right) + \beta \right) dq - \frac{c}{\sqrt{2\pi}} \int\_{-\xi / \sqrt{2\eta}}^{\infty} e^{-\frac{1}{2} q^2} dq
\end{aligned} $$

where

$$ \begin{aligned}
\alpha &= \dfrac{\sigma^2 \sqrt{\eta / 2}}{r - \frac{1}{2} \sigma^2} = \sigma \sqrt{T - t} ~, \\\\
\text{and } ~ ~ \beta &= \dfrac{\frac{1}{2} \sigma^2 \xi}{r - \frac{1}{2} \sigma^2} = \log\left( \dfrac{S}{c} \right) + \left(r - \dfrac{1}{2} \sigma^2 \right) (T - t) ~,
\end{aligned} $$

now

$$ \begin{aligned}
y(\xi,\eta) &= \frac{c}{\sqrt{2\pi}} e^{\beta + \frac{1}{2} \alpha^2} \int\_{- \xi / \sqrt{2\eta}}^{\infty} e^{-\frac{1}{2} (q - \alpha)^2} dq - \frac{c}{\sqrt{2\pi}} \int\_{-\infty}^{\xi / \sqrt{2\eta}} e^{-\frac{1}{2} q^2} dq \\\\
&= c e^{\beta + \frac{1}{2} \alpha^2} \int\_{-\infty}^{ \xi / \sqrt{2\eta} ~ ~ + \alpha} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2} q^2} dq - c \int\_{-\infty}^{\xi / \sqrt{2\eta}} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2} q^2} dq \\\\
&= c e^{\beta + \frac{1}{2} \alpha^2} \Phi \left( \frac{\xi}{\sqrt{2\eta}} + \alpha \right) - c \Phi\left(\frac{\xi}{\sqrt{2\eta}} \right) ~,
\end{aligned} $$

where $\Phi (z) = \int\_{-\infty}^{z} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2} q^2} dq$ is the cumulative normal distribution function.
