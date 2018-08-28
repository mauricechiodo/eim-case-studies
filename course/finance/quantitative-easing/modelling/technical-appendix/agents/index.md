---
Title: Agents and the Equations that Govern them
Template: ListSubPages
---

# Agents
$\newcommand{\F}[1]{^{[\text{F}#1]}}$$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$$\newcommand{\c}[1]{^{[#1]}}$$\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$
Agents are DSGE's representation of real-world active bodies - companies, households and government. They act according to their own needs, restrictions and with a goal in mind - typically the goal of maximising money made.

## [Households](course/finance/quantitative-easing/modelling/technical-appendix/agents/households)

Households are meant to be literally houses, representing workers that monopolistically supply labour, consume and enjoy leisure. Households also invest in bonds. Unrestricted households ($u$) can invest in both long- and short-term bonds, but suffer a transaction cost $\zeta\_t$ for every unit of long-term bond they purchase. Restricted households ($r$) can only invest in long-term bonds, but suffer no such transaction cost.

Each household supplies labour, the type of which is indexed as a continuum $i\in[0,1]$. They each have their own preferences (for working hours, types of items consumed etc), their own habit and aversion to risk. The households have utility at each time step, a budget constraint$\F{1}$ and a wage they want to optimise to get most income over all time. The supply of their labour type and elasticity of it informs labour agencies about how to price labour.

## [Labour Agencies](course/finance/quantitative-easing/modelling/technical-appendix/agents/labour-agencies)

Labour Agencies combine the differentiated labour inputs from households into a composite labour force. The value of this composite helps inform the demand for each different type of labour. Labour which is higher in demand will have higher compensation and be more attractive.

Labour agencies have a **zero profit condition**, which means that there is a very low cost of entry into the business such that there is a large supply into the business and so the market becomes perfectly competitive. The most famous example is the gold rushes. Under this condition the aggregate wage index (a measure of how high wages are in general) is only a function of the wage set by the $i^{th}$ household.

### Wage Setting

Households, being the monopolistic suppliers of labour, set wages. Since it is costly to reset wages every time step$\F{2}$, at each time step the chnace of resetting a wage is $1-\zeta\_w$. If the wage is not reset it automatically increases by a factor of $\Pi e^\gamma$.$\F{3}$ Households seek to maximise their profit over all time, accounting for the fact that if they set the wage too high they may lose out due to others setting a lower wage.

While households do not literally set their own wages in the real world, this is a reflection of them chosing a place to work based on the labour they supply and how much they value their labour.

## [Capital Producers](course/finance/quantitative-easing/modelling/technical-appendix/agents/capital-producers)

Capital Producers are agents that imperfectly manage a real amount of capital $\bar{K}\_t$ and use it, on behalf of their shareholders.$\F{4}$ They generate capital by investing an amount in the market. It is assumed that adjusting investment is costly and that any real capital not invested is depreciated at each time step. The objective of capital producers is to maximise the expected dividends to their shareholders over all time (which is implicitly the most profitable course for them).

## [Goods Producers](course/finance/quantitative-easing/modelling/technical-appendix/agents/goods-producers)

Goods producers take a continuum of inputs (indexed by $i\in[0,1]$) and aggregate them into some good. Each is attempting to maximise profits and has a resource constraint based on the total resources available in the economy.$\F{5}$

### Intermediate Goods Producers

Intermediate goods producers, indexed by $f\in[0,1]$, takes a single type of labour input (from households that supply labour type $f$) and transform it in a technology-augmented process into an intermediate good of type $f$. The intermediate goods producer also sets prices on a staggered basis (as with household's wages) with probability $1-\zeta\_p$ in order to maximise expected profits over all time.

### Final Goods Producers

Final goods producers take the entire continuum of intermediate goods and combine it into a homogenous final good that is consumed by households. The aggregate price index can be calculated based on the demands for different intermediate goods and the supply of each one.

## [Government Policies](course/finance/quantitative-easing/modelling/technical-appendix/agents/government)

The government represents the central bank and the influence that has on the market. It is assumed that the government can affect interest rates and spends all money available to them.$\F{6}$ The government also supplies all long-term bonds.

---

# Footnotes

$\F{1}$ The constraint of having a finite amount of wealth while existing is costly.

$\F{2}$ Imagine if a company changed the wages of every employee every day to account for demand, labour elasticity and so forth - the administrative force required would be huge, and costly.

$\F{3}$ $\Pi e^\gamma$ is the amount of inflation and the rate at which products are growning.

$\F{4}$ Exclusively households.

$\F{5}$ This is modelled as a *global* resource constraint under the assumption that goods producers will use all available resources in the whole system.

$\F{6}$ The budget constraint inequality becomes an equality.

---
