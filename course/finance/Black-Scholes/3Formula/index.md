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
&= c e^{\beta + \frac{1}{2} \alpha^2} \int\_{-\infty}^{ \xi / \sqrt{2\eta} ~ + \alpha} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2} q^2} dq - c \int\_{-\infty}^{\xi / \sqrt{2\eta}} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2} q^2} dq \\\\
&= c e^{\beta + \frac{1}{2} \alpha^2} \Phi \left( \frac{\xi}{\sqrt{2\eta}} + \alpha \right) - c \Phi\left(\frac{\xi}{\sqrt{2\eta}} \right) ~,
\end{aligned} $$

where $\Phi (z) = \int\_{-\infty}^{z} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2} q^2} dq$ is the cumulative normal distribution function.

Finally, computing

$$ \begin{aligned}
\frac{\xi}{\sqrt{2\eta}} &= \frac{1}{\sigma \sqrt{T - t}} \left( \log \left( \frac{S}{c} \right) + \left( r - \frac{1}{2} \sigma^2 \right) (T - t) \right) \\\\
\text{and} ~ ~ ce^{\beta + \frac{1}{2} \alpha^2} &= S e^{r(T-t)} ~,
\end{aligned} $$

we arrive at the Black-Scholes formula for a European call option:

> $$ \begin{aligned}
> V(S,t) &= S \Phi (d\_1) - ce^{-r(T-t)} \Phi (d\_2) ~, \\\\
> \text{where} ~ ~ d\_1 &= \frac{1}{\sigma \sqrt{T - t}} \left( \log \left( \frac{S}{c} \right) + \left( r + \frac{1}{2} \sigma^2 \right) (T - t) \right) ~, \\\\
> \text{and} ~ ~ d\_2 &= \frac{1}{\sigma \sqrt{T - t}} \left( \log \left( \frac{S}{c} \right) + \left( r - \frac{1}{2} \sigma^2 \right) (T - t) \right) ~.
> \end{aligned} $$

Without too much more work, we can also consider a European put option $U$ with the same parameters: this has payout

$$ U(S,T) = \begin{cases}
0 &  \text{if } S \geqslant c \\\\
c - S & \text{if } S < c
\end{cases} ~; $$

we see that $V(S,T) - U(S,T) = S - c$ for all $S$ (where $V$ is the value of a European call option, as found above). Using similar transformations as before, this gives that

$$ \begin{aligned}
V(S,t) - U(S,t) &= \frac{c e^{-r(T-t)} }{\sqrt{2\pi}} \int\_{\infty}^{\infty} \left( \exp \left( \frac{1}{2} \sigma^2 ( \xi + q \sqrt{2\eta} ) \big/ \left(r - \frac{1}{2} \sigma^2 \right) \right) - 1 \right) e^{-\frac{1}{2} q^2} dq \\\\
&= e^{-r(T-t)} \left( ce^{\beta + \frac{1}{2} \alpha^2} \int\_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2} (q - \alpha)^2} dq - c \int\_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2} q^2} dq \right) \\\\
&= e^{-r(T-t)} \left( ce^{\beta + \frac{1}{2} \alpha^2} - c \right) \\\\
&= S - ce^{-r(T-t)} ~,
\end{aligned} $$

(where $\alpha$ and $\beta$ are as before) and so, using the identity $1 - \Phi(z) = \Phi(-z)$, we get the Black-Scholes formula for a European put option:

> $$ U(S,t) = -S \Phi (-d\_1) + ce^{-r(T-t)} \Phi (-d\_2) ~, $$

where $d\_1$ and $d\_2$ are as above.

---

Conceptually, the Black-Scholes formula is a powerful tool in financial mathematics: if we accept the [Black-Scholes model](1Model) for the market, and the assumptions about the trading strategies of agents in the markets, the formula takes a **stochastic** model for the market and produces a **deterministic** formula for how to price certain items in the market. Not only that, but the formula is somewhat simple.

This is another place where problems can arise: in order to *use* this formula, all one needs is a scientific calculator, and some values for the interest rate $r$ and volatility $\sigma$. In order to *interpret* the [Black-Scholes equation](2Equation) or the formula one needs to have some knowledge of economics, the concepts of portfolio hedging and 'moneyness', and the behaviour of the stock market. But in order to fully *understand* the formula, one must have knowledge of the derivation; and this requires some advanced mathematics: (among other things) stochastic calculus and the diffusion equation.

As a principle
> If we don't know the **derivation**,  
> then we can't know the **limitations**.

And this is quite pervasive in mathematical modelling: making assumptions allows you to overlook inconvenient features of a real-world situation which could be difficult to incorporate into your model, or prevent you from deriving closed form solutions; but as a consequence, your model may no longer reflect the real world as faithfully. And when mathematicians develop models based on such assumptions, there is a need to be transparent about them, so that anyone using the model can appreciate how accurate it can be expected to be, how robust (or not) it may be, and what real-world phenomena the model may not account for.

---

To read about some real world phenomena that the Black-Scholes model doesn't account for equation, check out [the risks](4Risks).
