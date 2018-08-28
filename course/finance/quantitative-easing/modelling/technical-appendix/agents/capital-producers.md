---
Title: Capital Producers
Template: LeafPage
---

# Capital producers
$\newcommand{\F}[1]{^{[\text{F}#1]}}$$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$$\newcommand{\c}[1]{^{[#1]}}$$\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$
-   $u\_t$ is the **utilization rate**, how efficiently a company can
    use their capital.

-   $K\_t$ is **effective capital**, their capital having considered
    utilization rate. If a company is only 50% efficient with their
    money then having £100 is as good as a 100% efficient company having
    £50.

-   $\delta\in(0,1)$ is the **depreciation rate**, indication how
    quickly real capital becomes devalued.

-   $\mu\_t$ is an **investment specific technology shock**, a shock
    that is based on the unexpected development of technology that can
    make a company more efficient.

-   $S(f(t))$ is the **cost of adjusting investment**, how expensive
    it is to change your investment portfolios as the market changes.
    The function obeys $S'(\cdot))\geq0$ and $S''(\cdot)>0$. It is
    further assumed that $S(e^\gamma)=S'(e^\gamma)=0$.

-   $\Xi\_{t+s}^p$ is the **future profits discount** that occurs
    because the value of perpetuities held by their shareholders reduce
    in value over time.

-   $I\_t$ is the **capital from investment** that is acquired by a
    capital producer.

Effective capital for a competitive capital producer is based on the
real capital that the producer already has times their utilization rate.

$$K\_t=u\_t\bar{K}\_{t-1}$$

Capital producers accumulate capital based on the capital they already
have being depreciated plus the additional capital they acquire from
investment.

$$\bar{K}\_t=(1-\delta)\bar{K}\_{t-1}+\mu\_t\left[1-S\left(\frac{I\_t}{I\_{t-1}}\right)\right]I\_t$$

The discount of profits due to the individual discount factors of its
shareholders (households) is identically:

$$\Xi\_{t+s}^p\equiv\omega\_u\beta\_u^s\Xi\_{t+s}^{u,p}+\omega\_r\beta\_r^s\Xi\_{t+s}^{r,p}$$

Capital producers maximise the expected discounted stream of dividends
to their shareholders which is:

$$\mathbb{E}\_t \sum\_{s=0}^\infty\Xi\_{t+s}^p\left[R\_{t+s}^k u\_{t+s} \bar{K}\_{t+s-1}-P\_{t+s}a\left(u\_{t+s}\right)\bar{K}\_{t+s-1}-P\_{t+s}I\_{t+s}\right]$$
