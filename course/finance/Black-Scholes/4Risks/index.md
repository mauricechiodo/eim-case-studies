---
Title: The Risks
Template: LeafPage
---

# The Risks

Here we detail some of the particular risks overlooked by the assumptions of the [Black-Scholes model](course/finance/Black-Scholes/1Model):

- <a href="https://www.investopedia.com/terms/t/tailrisk.asp" target="_blank">*Tail risk:*</a> This is a form of portfolio risk that arises when the possibility that an investment will mve more than three standard deviations from the mean is greater than what is shown by a normal distribution. By using the <a href="/course/course/finance/Black-Scholes/Brownian-motion" target="_blank">geometric Brownian motion</a>, we have implicitly assumed that the distribution of percentage returns on the underlying stock is normal; this underpins the resulting [formula](course/finance/Black-Scholes/3Formula), but some analyses of market data have suggested that this doesn't hold. Specifically, the markets analysed displayed skew (when a distribution is asymmetric about the mean) and leptokurtosis (when the tails of a distribution are 'fatter' than those of a normal distribution). As a result, in these markets the BLack-Scholes model would underestimate the probability of large fluctuations in stock price.

- <a href="https://www.investopedia.com/terms/l/liquidityrisk.asp" target="_blank">*Liquidity risk:*</a> The risk that stems from the lack of marketability of investments that cannot be bought or sold quickly enough to prevent or minimise a loss - the assumption of instant, cost-less trading ignores this risk. A particularly extreme example of this was 'Francogeddon' in the foreign exchange market (one of the most liquid markets there is), in which the Swiss National Bank abandoned a cap on the franc-euro exchange rate, which had up until then been implemented for three years. On the day that this was announced, the daily range of the franc was equal to $31,000 per single futures contract, which is more than the market had previously moved collectively in the previous *thousand days* of trading.

- <a href="https://www.investopedia.com/terms/g/gaprisk.asp" target="_blank">*Gap risk:*</a> When a security's price changes from one level to another with no trading in between - the assumption of continuous trading (and of continuous time) ignores this possibility. For example, adverse news announcements after a particular day's trading might cause a stock price to drop substantially from the previous day's closing price.

- *Volatility risk:* finally, the model assumes a constant volatility of the <a href="/course/course/finance/Black-Scholes/Brownian-motion" target="_blank">Brownian motion</a>. In fact, given a price for a particular option, the Black-Scholes formula can be solved (numerically) to find the implied volatility. This implied volatility *should* be constant (for a particular stock) over all strike prices and maturities but in practice it isn't. For example, with respect to strike prices: equities tend to have skewed curves where, compared to 'at-the-money', implied volatility is higher for low strike prices, and lower for high strike prices; commodities are often skewed in the opposite way; and currencies, while giving typically more symmetrical curves, tend to have lowest volatility at-the-money, and higher volatility to both sides.

---

So, [why does this matter](course/finance/Black-Scholes/Ethics)?

---
