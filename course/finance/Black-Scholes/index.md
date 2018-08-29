---
Title: Option Pricing
Template: LeafPage
---

> "How did the biggest financial train wreck in human history come about?  
> Arguably, one contributor was a mathematical equation."  

 ~ Professor Ian Stewart, *In pursuit of the Unknown: 17 Equations That Changed the World*

---

# Option Pricing: The Black Scholes Equation

 - <a href="https://cueimps.soc.srcf.net/course/course/finance/Black-Scholes/Options" target="_blank">*Option:*</a> A type of financial derivative sold by an option writer to an option buyer. It is a contract offering the buyer the right, but not the obligation, to buy (if it is a *call* option) or to sell (if it is a *put* option) a particular underlying asset (or 'stock') at an agreed-upon price, during a certain period of time, or on a specific date. The agreed upon price is called the *strike price*. If the buyer chooses to utilise their right to buy or to sell the underlying asset, we say the option is *exercised*.

In 1973, Fischer Black and Myron Scholes derived an equation for pricing options; the equation describes how the price should evolve as a function of time and the current market price of the stock. It also takes into account the 'risk-free interest rate' of the market, and the 'volatility' of the stock.

Black and Scholes were by no means the first to apply mathematics to the stock market - that claim lies with Louis Bachelier, a french mathematician who in 1900 wrote his PhD thesis, *Théorie de la spéculation* \[1\], on the behaviour of stock prices and how to price derivative contracts - nor were they the first to create options pricing formulae: in their own paper, they reference multiple papers predating theirs, each giving some form of valuation formula.

What was revolutionary about Black and Scholes' formula was that it was, in some sense, 'complete'.  
For example, Black and Scholes write
> "Sprenkle's formula for the value of an option can be written as follows:
>
> $$ \begin{aligned}
> & kx N(b_1) - k^\* c N(b_2) \\\\
> b_1 &= \frac{\ln kx/c + \frac{1}{2} v^2 (t^\* - t)}{v\sqrt{t^\* - t}} \\\\
> b_2 &= \frac{\ln kx/c - \frac{1}{2} v^2 (t^\* - t)}{v\sqrt{t^\* - t}}
> \end{aligned} $$
> 
> In this expression, $x$ is the stock price, $c$ is the exercise price, $t^\*$ is the maturity date, $t$ is the current date, $v^2$ is the variance rate of the return on the stock, $\ln$ is the natural logarithm, and $N(b)$ is the cumulative normal density function. But $k$ and $k^\*$ are unknown parameters. Sprenkle (1961) defines $k$ as the ratio of the expected value of the stock price at the time the warrant matures to the current stock price, and $k^\*$ as a discount factor that depends on the risk of the stock. He tries to estimate the values of $k$ and $k^\*$ empirically, but finds that he is unable to do so."  

 ~ Fischer Black and Myron Scholes, *The Pricing of Options and Corporate Liabilities*, Journal of Political Economy, May 1973.

The Black-Scholes' formula is identical in form to Sprenkle's, except that Black and Scholes derived explicit expressions for $k$ and $k^\*$.

---

Read more about the Black-Scholes model for financial markets, the equation they derived, the formula that solves it, and some of the risks behind all of these:

 <div id=grid>
 
 <a href="https://cueimps.soc.srcf.net/course/course/finance/Black-Scholes/1Model">
 <img src="http://cueimps.soc.srcf.net/course/media/B-S/1Model.jpg"/>
 </a>
 
 <a href="https://cueimps.soc.srcf.net/course/course/finance/Black-Scholes/2Equation">
 <img src="http://cueimps.soc.srcf.net/course/media/B-S/2Equation.jpg"/>
 </a>
 
 <a href="https://cueimps.soc.srcf.net/course/course/finance/Black-Scholes/3Formula">
 <img src="http://cueimps.soc.srcf.net/course/media/B-S/3Formula.jpg"/>
 </a>
 
 <a href="https://cueimps.soc.srcf.net/course/course/finance/Black-Scholes/4Risks">
 <img src="http://cueimps.soc.srcf.net/course/media/B-S/4Risks.jpg"/>
 </a>

 </div>

---

\[1\] - L. Bachelier, *Théorie de la spéculation*, Annales scientiﬁques de l’École normale supérieure, 17:21–86, 1900.
