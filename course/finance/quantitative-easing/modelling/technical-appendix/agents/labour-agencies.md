---
Title: Labour Agencies
Template: LeafPage
---

# Labour Agencies and Wage Setting Decision
$\newcommand{\F}[1]{^{[\text{F}#1]}}$$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$$\newcommand{\c}[1]{^{[#1]}}$$\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$
-   $\lambda\_w\geq0$ is the **steady state wage markup** - the
    amount that a non-sticky$\F{1}$ wage would be increased during
    constant inflation. “Steady state" refers to the assumption that
    there is a constant stock of physical wealth and a constant
    population.

-   $L\_t$ is the **homogenous labour composite**, the collection of
    labour as an abstract force.

-   $W\_t$ is the **aggregate wage index**; this is approximately the
    average wage.

-   $\Pi$ is the steady state **rates of inflation**

-   $e^\gamma$ is the steady state **rate of product growth**, the
    rate at which the amount of products grows.

-   $\zeta\_w\in[0,1]$ is the **probability** that **wage doesn’t
    reset** in a given time period. A wage ‘resetting’ is just it
    being adjusted in some way, typically for inflation.

-   $\tilde{W}\_t^j(i)$ is the **wage chosen** at time $t$ in the
    event of an adjustment.

-   $\Xi\_t^{j,p}$ is the **marginal utility of consumption** in
    nominal terms. The marginal utility is the *change* in utility
    when $t\mapsto t+1$. The utility of consumption is the utility
    generated from consuming, as, for example, shown in the equation for
    a household’s utility over its lifetime.

Labour agencies (agents that assign labour to companies) combine
differentiated labour inputs indexed by $i$ into a composite $L\_t$
through the formula

$$L\_t=\left[\int\_0^1 L\_t(i)^{\frac{1}{1+\lambda\_w}}di\right]^{1+\lambda\_w}$$

To maximise profit, the demand for the $i^{th}$ labour input becomes

$$L\_t(i)=\left[\frac{W\_t(i)}{W\_t}\right]^{-\frac{1+\lambda\_w}{\lambda\_w}}L\_t$$

Labour agencies have a **zero profit condition**, which means that
there is a very low cost of entry into the business such that there is a
large supply into the business and so the market becomes perfectly
competitive. The most famous example is the gold rushes. Under this
condition the aggregate wage index is a function of wage set by the
$i^{th}$ household.

$$W\_t=\left[\int\_0^1W\_t(i)^{-\frac{1}{\lambda\_w}}di\right]^{-\lambda\_w}$$

## Wage Setting

Households have a monopoly on labour input, and set wages on a staggered
basis. In each period, the probability of resetting the wage is
$1-\zeta\_w$, and if the wage is not reset it automatically increases by
$\Pi e^\gamma$. Thus

$$W\_{t+s}^j(i)=(\Pi e^\gamma)\tilde{W}\_t^j(i)$$.

The household will chose $\tilde{W}\_t^j(i)$ to maximise the expression

$$\mathbb{E}\_t\sum\_{s=0}^\infty(\beta\_j\zeta\_w)^s\left[\Xi\_{t+s}^{j,p}\tilde{W}\_t^j(i)L\_{t+s}^j(i)-\frac{\varphi\_{t+s}^j(L\_{t+s}^j(i))^{1+\nu}}{1+\nu}\right]$$,

that is to say, they will maximise the wage as much as possible while
not overcharging for their labour. If the household works a particularly
elastic job, they will set their wage to be less than if they worked a
very inelastic job. Of course, in the real world each individual
household does not declare what they will charge and then demand this
from their boss. Rather, this optimisation is the understanding that
generally a household will implicitly do this by choosing where to work.
When there are billions of households this becomes the general trend.

---

# Footnotes

$\F{1}$ A sticky wage keeps the same nominal value or close to the same nominal value despite inflation.
