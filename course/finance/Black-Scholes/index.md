---
Title: The Black-Scholes Equation
Template: ListSubPages
---

"*How did the biggest financial train wreck in human history come about?*  
*Arguably, one contributor was a mathematical equation.*"  
> ~ Professor Ian Stewart ~ "In pursuit of the Unknown: 17 Equations That Changed the World"
     
# The Black-Scholes Equation

In 1973, Fischer Black and Myron Scholes derived an equation for option pricing; the equation describes how the price of an option should evolve as a function of time and the current market price of the stock. It also takes into account the 'risk-free interest rate' and the 'volatility' of the stock.

Black and Scholes were by no means the first to apply mathematics to the stock market - that claim lies with Louis Bachelier, a french mathematician who in 1900 wrote his PhD thesis, *Théorie de la spéculation*, on the behaviour of stock prices and how to price derivative contracts - nor were they the first to create options pricing formulae: in their own paper, they reference multiple papers predating theirs, each giving some form of valuation formula.

What was revolutionary about Black and Scholes' formula was that it was, in some sense, 'complete'. For example, Black and Scholes write
> "*Sprenkle's formula for the value of an option can be written as follows:*"
 
\begin{align*}
& kx N(b_1) - k^* c N(b_2) \\
b_1 &= \frac{\ln kx/c + \frac{1}{2} v^2 (t^* - t)}{v\sqrt{t^* - t}} \\
b_2 &= \frac{\ln kx/c - \frac{1}{2} v^2 (t^* - t)}{v\sqrt{t^* - t}}
\end{align*}
