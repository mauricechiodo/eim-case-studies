---
Title: Goods Producers
Template: LeafPage
---

# Intermediate goods producers
$\newcommand{\F}[1]{^{[\text{F}#1]}}$$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$$\newcommand{\c}[1]{^{[#1]}}$$\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$
-   $Z\_t$ is a **labour-augmented technological process** - a method
    by which technology increases the amount of value created. (Consider
    how much more efficient labour is with the advent of computers)

-   $\zeta\_p$ the **probability of no price adjustment** for
    intermediate goods producers per unit time.

-   $\lambda\_{f,t}$ is a **goods markup shock**, a shock governing
    the unexpected increase in cost of production relative to its price.

-   $\alpha$ is the **share of capital in production**, how much
    your capital matters for production versus the amount of labour.
    This is constant among all companies and is a reflection of the
    state of goods production in the world, rather than being
    individualised per type of intermediate good. In MELP $\alpha=0.33$.

An intermediate goods producer, indexed by $f\in[0,1]$ produces
intermediate goods based on their effective capital and labour put in.

$$Y\_t(f)=K\_t(f)^\alpha(Z\_tL\_t(f))^{1-\alpha}$$

The labour-augmented technology evolves with the difference equation

$$log\left(\frac{Z\_t}{Z\_{t-1}}\right)=(1-\rho\_z)\gamma+\rho\_zlog\left(\frac{Z\_{t-1}}{Z\_{t-2}}\right)+\epsilon\_{z,t}$$

that is to say,

$$Z\_t=e^{(1-\rho\_z)\gamma+\rho\_z+\epsilon\_{z,t}}\frac{Z\_{t-1}^2}{Z\_{t-2}}$$

The marginal cost, the increase in cost per unit time, can be deduced
from aggregate variables

$$MC(f)\_t=MC\_t=\frac{(R\_t^k)^\alpha W\_t^{1-\alpha}}{\alpha^\alpha (1-\alpha)^{1-\alpha}Z\_t^{1-\alpha}}$$

A firm can set prices on a staggering basis with probability $1-\zeta\_p$
independantly of past successes. When a firm can adjust, they will
maximise $\tilde{P}\_t(f)$ assuming no further adjustments can be made,
so maximising their profit

$$\mathbb{E}\_t\sum\_{s=0}^\infty   \zeta\_p^s\Xi\_{t+s}^p\left[\tilde{P}\_t(f)\Pi^s-\lambda\_{f,t+s}MC\_{t+s}\right]Y\_{t+s}(f)$$

# Final Goods Producers

-   $Y\_t(f)$ is an **intermediate good** indexed by $f\in[0,1]$

-   $\lambda\_f\geq0$ is the **steady state price markup**.

The final goods producer will combine different intermediate goods
$Y\_t(f)$ into a homogeneous good $Y\_t$

$$Y\_t = \left[ \int\_0^1 Y\_t(f)^{\frac{1}{1+\lambda\_f}}df\right]^{1+\lambda\_f}$$

Therefore, the demand for the $f^{th}$ intermediate good is (relative to
aggregate price index $P\_t$ and the price set by the $f^{th}$
intermediate goods producer) derived to be the
following.$\c{1}$

$$Y\_t(f)=\left[\frac{P\_t(f)}{P\_t}\right]^{-\frac{1+\lambda\_f}{\lambda\_f}}Y\_t$$

From the zero-profit condition for intermediate goods producers the
aggregate price index $P\_t$ is as follows

$$P\_t=\left[\int\_0^1P\_t(f)^{-\frac{1}{\lambda\_f}}df\right]^{-\lambda\_f}$$

Meaning that final goods producers ultimately take a continuum of
intermediate goods and create some final good for which the price is
$P\_t$.
