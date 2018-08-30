---
Title: Equilibrium and Solution Strategy
Template: LeafPage
---

# Equilibrium and Solution Strategy
$\newcommand{\F}[1]{^{[\text{F}#1]}}$$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$$\newcommand{\c}[1]{^{[#1]}}$$\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$
-   $\Xi\_t^u$ is the **marginal utility of detrended consumption**
    in real terms, the amount that the utility of consumption will
    change when $t\mapsto t+1$ in real terms.

In equilibrium, all households and firms maximise their own objectives,
with their own individual constraints. The resource constraint is

$$Y\_t=\omega\_uC\_t^u+\omega\_rC\_t^r+I\_t+G\_t+a(u\_t)\bar{K}\_{t-1}$$

This says that the amount of a homogenous final good at any moment must be
the amount consumed by households plus the amount invested in other
places.

Since unrestricted households are the only ones to trade in short-term
securities, the pricing equation for such a security is

$$1=\beta\_u\mathbb{E}\_t\left[e^{-\gamma-z\_{t+1}}\frac{\Xi\_{t+1}^u}{\Xi\_t^u}\frac{R\_t}{\Pi\_{t+1}}\right]$$

Both restricted and unrestricted households trade in long-term bonds,
the pricing of these for a household $j$ is

$$(1+\zeta\_t\mathbb{I}\_{\{j=u\}})=\beta\_j\mathbb{E}\_t\left[e^{-\gamma-z\_{t+1}}\frac{\Xi\_{t+1}^j}{\Xi\_t^j}\frac{P\_{L,t+1}}{P\_{L,t}}\frac{R\_{L,t+1}}{\Pi\_{t+1}}\right]$$

Where $\mathbb{I}$ is the indicator function.

## Transaction cost and the risk premium

-   $R\_{L,t}^{E H}$ is the **counterfactual yield to maturity** on a
    long-term bond in the absence of transaction costs

-   $D\_L$, in the context of equation (\[riskpremium\]), is the steady
    state **duration** of $\hat{R}\_{L,t}$ and $\hat{R}\_{L,t}^{EH}$

-   $\zeta\_t$ is the cost of transaction per unit for an unrestricted household for a long-term bond.

Theoretically, $R\_{L,t}^{EH}$ should have the same risk-adjusted return
as the actual long-term security. Therefore, the risk premium is
measured to a first order approximation between the two yields up to
maturity

$$\label{riskpremium}
    \hat{R}\_{L,t}-\hat{R}\_{L,t}^{EH}=\frac{1}{D\_L}\sum\_{s=0}^\infty\left(\frac{D\_L-1}{D\_L}\right)^s\mathbb{E}\_t\zeta\_{t+s}$$

The cost of transaction $\zeta\_t$ is not given an explicit form, but is
a function $\zeta$ of $P\_{L,t},B\_{z,t}^L$ and the error term
$\epsilon\_{\zeta,t}$,$\F{1}$ where identically
$B\_{z,t}^L\equiv B\_t^L/(P\_tZ\_t)$, ie

$$\zeta\_t\equiv\zeta(P\_{L,t}B\_{z,t}^L,\epsilon\_{\zeta,t})$$

## Limits to arbitrage

The concept of the restricted household is introduced in this paper in
order to try and break *Wallace’s Irrelevance Theorem*, which states
that in certain conditions, central banks buying securities won’t affect
the economy.$\c{1}$

Restricted households are the observation that there is a fraction of
the market which only purchases assets through long-term bonds, such as
pensions. The variable $\omega\_r$ captures this notion. The difference
between these types of households is meant to break Wallace and show
that QE is an effective strategy.

---

# Footnotes

$\F{1}$ $\zeta$ is specified to be strictly increasing and positive when evaluated in steady state, so $\zeta(P\_LB\_z^L,0)=0$ and $\zeta'(P\_LB_z^L,0)>0$.

---

# Bibliography

$\c{1}$ Wallace, Neil. "A Modigliani-Miller Theorem for Open-Market Operations." The American Economic Review 71, no. 3 (1981): 267-74. http://www.jstor.org/stable/1802777.
