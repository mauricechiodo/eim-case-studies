---
Title: Households
Template: LeafPage
---

# Households
$\newcommand{\F}[1]{$^{\text{F}#1}$}$
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

$$\mathbb{E}_t\sum_{s=0}^\infty\beta_j^s b_{t+s}^j \left[ \frac{1}{1-\sigma_j} \left( \frac{C_{t+s}^j}{Z_{t+s}}-h\frac{C_{t+s-1}^j}{Z_{t+s-1}} \right)^{1-\sigma_j} - \frac{\varphi_{t+s}^j(L_{t+s}^j(i))^{1+\nu}}{1+\nu} \right]$$

---

# Footnotes

$\F{1}$ A risk-averse person will favour a guaranteed £10, whereas one who is not risk averse will go for the £20. In extreme cases you have risk-loving and risk-fearing people, who will suffer some cost to $\mathbb{E}$(money) in order to take or not take risks. A risk-loving person may chose to get £15 50% of the time over £10 100% of the time.
