---
Title: The Black-Scholes model
Template: LeafPage
---

# The Black-Scholes model

In order to produce a formula for how to price options, we first need to describe the market; the financial setting within which we are trading.

Black and Scholes' market consists of one risky asset (the 'stock') and one riskless asset ('cash', or 'bond'). They then assume a set of "ideal conditions" in the market for the stock, and for an option on the stock as follows:

---

- The short-term interest rate is known and is constant through time.
- The stock price follows a random walk in continuous time with a variance rate proportional to the square of the stock price. Thus the distribution of possible stock prices at the end of any finite interval is log-normal. The variance rate of the return on the stock is constant.
- The stock pays no dividends or other distributions.
- The option is "European," that is, it can only be exercised at maturity.
- There are no transaction costs in buying or selling the stock or the option.
- It is possible to borrow any fraction of the price of a security to buy it or to hold it, at the short-term interest rate.
- There are no penalties to short selling. A seller who does not own a security will simply accept the price of the security from a buyer, and will agree to settle with the buyer on some future date by paying him an amount equal to the price of the security on that date.

---

Many of these assumptions are for mathematical simplicity: for example, not all options are European, but the restriction that a European option may only be exercised at its maturity date allows for an equation - for 'American' option, which may be exercised any time *up to* and including its maturity, the Black-Scholes' equation becomes an inequality.

However, some of these implicitly make assumptions on human behaviour and society: modelling the stock price as having a particular distribution for example; the stock price is affected by how people are buying and selling the stock, so an assumption on stock price distribution is an assumption on the actions of market agents.

And here we see a potential problem of mathematical models on financial markets:
>  ***The act of modelling the market may affect the market.***

Another point to note is that Black and Scholes arrived at their famous equation by assuming that market agents take a particular type of 'hedged position', where (having bought or sold an option) they buy and sell the underlying stock in just the right quantities, such that their total portfolio value remains unaffected by changes in the stock price. This is a second assumption on the behaviour of traders, and may not be compatible with the distribution assumption.

To read about the Black Scholes equation and how it can be derived click here:
- [The equation](2Equation)  
To read more about the risks of the model, the equation, and the formula, click here:
- [The risks](4Risks)
