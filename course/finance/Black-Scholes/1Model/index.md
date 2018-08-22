---
Title: The Black-Scholes model
Template: LeafPage
---

# The Black-Scholes model

In order to produce a formula for how to price options, we first need to describe the market; the financial setting within which we are trading.

Black and Scholes' market consists of one risky asset (the 'stock') and one riskless asset ('cash', or 'bond'). They then assume a set of "ideal conditions" in the market for the stock, and for an option on the stock as follows:

- The short-term interest rate is known and is constant through time.
- The stock price follows a random walk in continuous time with a variance rate proportional to the square of the stock price. Thus the distribution of possible stock prices at the end of any finite interval is log-normal. The variance rate of the return on the stock is constant.
- The stock pays no dividends or other distributions.
- The option is "European," that is, it can only be exercised at maturity.
- There are no transaction costs in buying or selling the stock or the option.
- It is possible to borrow any fraction of the price of a security to buy it or to hold it, at the short-term interest rate.
- There are no penalties to short selling. A seller who does not own a security will simply accept the price of the security from a buyer, and will agree to settle with the buyer on some future date by paying him an amount equal to the price of the security on that date.
