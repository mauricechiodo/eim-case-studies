---
Title: Households
Template: LeafPage
---

# Households
$\newcommand{\F}[1]{^{[\text{F}#1]}}\newcommand{\c}[1]{^{[#1]}}\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$
## Utility

* A household is the monopolistic supplier of labour in the market, they can be restricted ($r$), or unrestricted ($u$), let $j\in\\{u,r\\}$ – a restricted household cannot trade in short-term bonds.
* $C\_t^j$ is a household’s **consumption** relative to **productivity** $Z\_t$, how many resources (food clothes etc) that the household consumes. This is relative to the total productivity of the economy.
* $L\_t^j$ is a household’s hours worked per unit time.
* Households supply differentiated labour inputs indexed by i, that is to say the different types of labour required are modelled as a continuum, $i\in[0,1]$.
* $\beta\_j\in(0,1)$ is the individual discount factor - this is the devaluing of an asset’s future income, accounting for having to wait for the asset to mature.
* $b\_t^j$ is a preference shock - a shock is an unexpected change, and a preference shock is an individual choosing one thing over another suddenly, eg consumption over leisure. This will alter utility and so is represented by a random variable at each timestep.
* $\sigma\_j>0$ is the coefficient of relative risk aversion, a higher $\sigma\_j$ indicates that the household is more risk-averse, eg they would prefer to be given £10 100% of the time rather that £20 50% of the time.$\F{1}$
* $h\in(0,1)$ is the habit parameter - an increase in current consumption lowers the marginal utility of consumption in the current period and increases it in the next period. Intuitively, the more the consumer eats today, the hungrier they wake up tomorrow.
* $\nu\geq0$ is the inverse elasticity of labour supply - labour being elastic ($\nu\ll1$) implies that labour will come and go as compensation changes. An inelastic job would have the same workforce even with wage changes.
* $\varphi\_t^j$ is a labour supply shock - unexpected changes in labour supplied.

The lifetime utility of a household is given as the equation

$$\mathbb{E}\_t\sum\_{s=0}^\infty\beta\_j^s b\_{t+s}^j\left[\frac{1}{1-\sigma\_j}\left(\frac{C\_{t+s}^j}{Z\_{t+s}}-h\frac{C\_{t+s-1}^j}{Z\_{t+s-1}}\right)^{1-\sigma\_j}-\frac{\varphi\_{t+s}^j(L\_{t+s}^j(i))^{1+\nu}}{1+\nu}\right]$$

This equation is composed of several, individually simple parts summed over time. At each time interval it looks at the consumption relative to productivity the household performs, minus the habit parameter times last time interval's consumption (this is the waking up hungrier). That function is then modified dependant on how risk-averse the household is. It then subtracts the amount of labour provided in hours worked (with some function related to the elasticity applied) that is multiplied by the shock of labour supply.

Then at each step the total utility is devalued by $\beta\_j^s$ (recall $\beta\_j\in(0,1)$ so $\beta\_j^s\to0$ as $s\to\infty$) and multiplied by the preference shock at that time.

This is summed over all time, creating the total utility.

---

## Budget Constraint

-   **Short-term bonds** are purchased for $B_t$ at time $t$ and
    have a nominal$\F{2}$ return of $R_t$ at time $t+1$

-   **Long-term bonds** are perpetuities (bonds that last forever)
    that cost $P_{L,t}$ at time $t$ and make returns proportional to
    $\kappa^s$ at time $t+s+1$, $\kappa\in(0,1]$ so at each stage the
    returns they make decays and tends to 0.

-   $\omega_u$ is the proportion of unrestricted households,
    $\omega_r=1-\omega_u$.

-   $\zeta_t$ is the **transaction cost per unit** of long-term
    bonds purchased by unrestricted households, so the amount it costs
    an unrestricted household to purchase a long-term bond. This may be
    fees from, say, a hedge-fund manager.

-   $P_t$ is the price of the **final consumption good**. This is
    the simplification of all consumption costs, food, medicine, rent
    etc. To find the amount spent on consumption by a household the
    expression would be $P_tC_t^j$.

-   $W_t^j(i)$ is the **wage** set by a household of type $j$ who
    supplies labour of type $i$, that is to say the wage of that
    household. Different types of labour and different types of
    household will have different wages - doctors make different amounts
    to teachers.

-   $\mathcal{P}\_t^j$ and $\mathcal{P}\_t^{cp,j}$ are **profits**
    from ownership of **intermediate goods producers** and
    **capital producers** respectively. If a household happens to
    have stake in capital producers (factories, businesses) then this is
    the profit from that.

-   $T\_t^j$ are lump-sum taxes.

-   $R\_{L,t}$ is the **gross yield to maturity** at a time $t$ on
    the long term bond, the total money made before the bond matures.
    $R\_{L,t}=\frac{1}{P\_{L,t}}+\kappa$ is derived in the technical
    appendix.$\c{1}$

A budget constraint is the fundamental constraint of budgetting. If you
only have assets worth $K$ and $\exists$ a set of assets indexed by
$i\in\mathbb{A}$, and $\forall i\in\mathbb{A}, i$ costs $c_i$ and you
purchase $n\_i$ units of $i$, then necessarily
$$K\leq \sum\_{i\in\mathbb{A}}c\in i$$

Budget constraints differ based on if a household is restricted or
unrestricted. Unrestricted households can trade in both short and
long-term bonds, but pay $\zeta\_t$ per-unit of long-term bond purchased,
so the flow budget constraint is:

$$P\_tC\_t^u+B\_t^u+(1+\zeta\_t)P\_{L,t}B\_t^{L,u}\leq R\_{t-1}B\_{t-1}^u+\left(\sum\_{s=1}^\infty\kappa^{s-1}B\_{t-s}^{L,u}\right)+W\_t^u(i)L\_t^u(i)+\mathcal{P}\_t^u+\mathcal{P}\_t^{cp,u}-T\_t^u$$

For a restricted household that can only trade in long-term securities
and does not pay transaction costs, the flow budget constraint is:

$$P\_tC\_t^r+P\_{L,t}B\\_t^{L,r}\leq\left(\sum\_{s=1}^\infty\kappa^{s-1}B\_{t-s}^{L,r}\right)+\mathcal{P}\_t^r+\mathcal{P}\_t^{cp,r}+W\_t^r(i)L\_t^r(i)-T\_t^r$$

One advantage of assuming that the entire stock of long-term
government bonds consists of perpetuities is that the price in a
period $t$ of a bond issued $s$ periods ago $P_{L,t-s}$ is a function
of the coupon and the current price

$$P\_{L,t-s}=\kappa^sP\_{L,t}$$

This relation gives rise to a recursive formula, for which $\exists$ a
derivation.$\Ci{1}{Section A.4, p.8} The budget
constraints become:

$$P\_tC\_t^u+B\_t^u+(1+\zeta\_t)P\_{L,t}B\_t^{L,u}\leq R\_{t-1}B\_{t-1}^u+P\_{L,t}R\_{L,t}B\_{t-1}^{L,u}+W\_t^u(i)L\_t^u(i)+\mathcal{P}\_t^u+\mathcal{P}\_t^{cp,u}-T\_t^u$$

and

$$P\_tC\_t^r+P\_{L,t}B\_t^{L,r}\leq P\_{L,t}R\_{L,t}B\_{t-1}^{L,r}+\mathcal{P}\_t^r+\mathcal{P}\_t^{cp,r}+W\_t^r(i)L\_t^r(i)-T\_t^r$$

These dictate how many assets a household can buy based on how much
money they have available.

---

# Footnotes

$\F{1}$ A risk-averse person will favour a guaranteed £10, whereas one who is not risk averse will go for the £20. In extreme cases you have risk-loving and risk-fearing people, who will suffer some cost to $\mathbb{E}$(money) in order to take or not take risks. A risk-loving person may chose to get £15 50% of the time over £10 100% of the time.
