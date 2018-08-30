---
Title: Options
Template: ListSubPages
---

# Options

Options are contracts through which a seller gives a buyer the right, but not the obligation, 
to buy or sell a specified number of shares at a predetermined price within a set time period.
Some options specify the date at which the right to buy or sell must be exercised, others allow 
the buyer to exercise the right any time up to a specified date. 

The price, or cost, of an option is an amount of money known as the premium. The buyer pays the
premium to the seller in exchange for the right granted by the option. The buyer can then exercise
the option before the expiration date, or let the option expire (or it must be exercised on the expiration
date, depending on the type of option being traded). \cite{OptionsPricingBasics2012}.

Often a closed-form pricing formula either does not exist or is difficult to derive and therefore
numerical procedures are often used for valuing options.

A paper called "A numerical method for pricing spread options on LIBOR rates with a PDE 
model \cite{suarez-taboadaNumericalMethodPricing2010}" suggests one method for pricing spread options. 

A spread option is a type of option that derives its value from the difference, or spread, 
between the prices of two or more assets. In the paper, they present a new numerical method 
for solving a Black-Scholes type of model for pricing spread options based on Libor. The paper 
focusses on the statement of a PDE model for pricing a spread option contract which is obtained 
by using the Feynman–Kac theorem \footnote{This is a theorem which establishes a link between
parabolic partial differential equations and stochastic processes.} and goes on to provide 
numerical methods for solving this model to obtain an approximation for the spread options 
pricing. They state "The main advantage of PDE based pricing methods with respect to alternative
general purpose Monte Carlo ones is that they are computationally faster." 

We will now give an example of pricing options using a Monte Carlo method as described by 
a document entitled "Pricing complex options using a simple Monte Carlo 
Simulation \cite{finkPricingComplexOptions2004}" by Peter Fink. 

Once a basic pricing model has been constructed, it can be applied to different options 
simply by changing the pay-out function of the Libor variable $L$. There is no further 
need for complicated algebraic calculations.

The simulation is based on an algebraic expression with a stochastic term. The formula
generates paths for the Libor variable $L$ (note that other underlying variables instead 
of Libor can be used, such as a foreign exchange rate - here we have focussed on the formula 
which uses Libor) which are consistent with a given set of Libor rates (a forward rate is 
an interest rate applicable to a financial transaction that will take place in the future), 
volatilites and an assumed statistical distribution. 

We assume that the infinitesimal process for $L$ is given by 


$$dL=\mu Ldt + \sigma L dz$$


where $\mu$ is the expected proportional change in $L$ per unit time, $\sigma$ is the volatility of $L$ and $dz$ is 
the Wiener process $dz=\epsilon \sqrt{dt} $ where ($\epsilon \sim N(0,1)$), this is where the stochastic term comes 
from \footnote{The Wiener process $z(t)$ is a continuous-time stochastic process with the following properties:

- (Normal increments) $z(t)-z(s) \sim N(0,t-s)$
- Increments are independent on disjoint time intervals
- $z(t)$ is a continuous function of $t$
- $z(0)=0$

The notation $dz=\epsilon \sqrt{dt}$ is used to simplify the expression of a series of normal distributions, 
which is a Wiener process.}.

For a time interval starting at time $t$ and ending at time $T$, the generating formula for $L$ is given by 


$$L_{T}=L_{t} \times \frac{\text{ Foward LIBOR}_T}{\text{Forward LIBOR}_t} \times \exp\left({\left(-\frac{1}{2}\sigma^2\right)(T-t)+\sigma\epsilon\sqrt{T-t}}\right)$$


where we have used the fact that $\mu=\exp\left({\frac{\text{ Foward LIBOR}_T}{\text{Forward LIBOR}_t}}\right)$ for 
the Libor rate. Using this formula the pricing spreadsheet can now be assembled. 

This is how forward Libor rates are calculated \cite{davisFIXEDINCOMEPdf2002}:
First we define $p(s,t)$ which is equivalent to a simple interest payment of the 
Libor rate $L$ for the period $[s,t]$ by


$$p(s,t)=\frac{1}{1+\theta_{st}L}$$


where $\theta_{st}$ is known as the accural factor for the interval $[s,t]$. 
For $t<T_1<T_2$ the forward Libor rate $L^f(t;T_1,T_2)$ at $t$ for period $[T_1,T_2]$ is

$$L^f(t;T_1,T_2) = \frac{1}{\theta_{T_1T_2}}(\frac{p(t,T_1)}{p(t,T_2)}-1)$$
