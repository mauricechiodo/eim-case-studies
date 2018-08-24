---
Title: The Equation
Template: LeafPage
---

# The Black-Scholes Equation

> $$ \frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} + rS \frac{\partial V}{\partial S} - rV = 0 ~, $$
> where
> $V = V(S,t)$ is the price of the option as a function of the stock price $S$ and time $t$,  
> $r$ is the risk-free interest rate, and $\sigma$ is the volatility of the stock.

## Derivation:

The key assumption to Black and Scholes' work is that the underlying stock price $S$ follows a [geometric Brownian motion](course/finance/Black-Scholes/Brownian-motion) with drift $\mu$ and variance parameter $\sigma^2$. In the language of stochastic calculus, this states that

$$ dS = \mu S dt + \sigma S dW $$

where $W$ is a Brownian motion. Note that $W$ (and hence $dW$) is the only source of uncertainty here. Now with reagrds to $V(S,t)$, Itô's lemma (an important result in stochastic calculus) gives

$$ dV = \left( \frac{\partial V}{\partial t} + \mu S \frac{\partial V}{\partial S} + \frac{1}{2} \sigma^2 S^2 \frac{\partial ^2 V}{\partial S^2}\right) dt + \sigma S \frac{\partial V}{\partial S} dW ~. $$

Now we introduce a hedged portfolio that is [short](course/finance/Black-Scholes/Positions) one option (with value $V$), and [long](course/finance/Black-Scholes/Positions) $\frac{\partial V}{\partial S}$ shares at time $t$, the value $\Pi$ of these holdings is

$$ \Pi = -V + \frac{\partial V}{\partial S} S ~, $$

and over a time interval of length $\Delta t$, the profit (or loss) from changes in value of the holdings is

$$ \Delta \Pi = -\Delta V + \frac{\partial V}{\partial S} \Delta S ~. $$

Discretising the expressions for $dS$ and $dV$, we get

$$ \begin{aligned}
\Delta S &= \mu S \Delta t + \sigma S \Delta W \\\\
\Delta V &= \left( \frac{\partial V}{\partial t} + \mu S \frac{\partial V}{\partial S} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} \right) \Delta t + \sigma S \frac{\partial V}{\partial S} \Delta W ~,
\end{aligned} $$

and substituting these into the expression for $\Delta \Pi$ we find

$$ \begin{aligned}
\Delta \Pi &= - \left( \frac{\partial V}{\partial t} + \mu S \frac{\partial V}{\partial S} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} \right) \Delta t - \sigma S \frac{\partial V}{\partial S} \Delta W + \frac{\partial V}{\partial S} ( \mu S \Delta t + \sigma S \Delta W ) \\\\
&= -\left( \frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} \right) \Delta t ~.
\end{aligned} $$

Note that $\Delta W$ has now vanished; the portfolio is riskless, and thus the rate of return must be equal to  the rate of return on any other riskless instrument (else there would be the opportunity for arbitrage). As noted in Black and Scholes' [assumptions](course/finance/Black-Scholes/1Model), we assume that this risk-free interest rate is a known constant $r$, and so over the interval $\[ t, t + \Delta t \]$ we have

$$ r \Pi \Delta t = \Delta \Pi ~. $$

Then after substituting in the expressions for $\Pi$ and $\Delta \Pi$:

$$ r \left( -V + \frac{\partial V}{\partial S} S \right) \Delta t = -\left( \frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} \right) \Delta t ~. $$

Finally, cancelling the $\Delta t$'s and rearranging, we get the Black-Scholes equation:

$$ \frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} + rS \frac{\partial V}{\partial S} - rV = 0 ~. $$

---

To read about the solution to this differential equation, check out [the formula](course/finance/Black-Scholes/3Formula).
