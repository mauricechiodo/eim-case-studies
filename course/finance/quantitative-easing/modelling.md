---
Title: Macroeconomic Modelling
Template: LeafPage
---
$\newcommand{\F}[1]{^{\text{F}#1}}\newcommand{\c}[1]{^{[#1]}}\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$
## Modelling

Macroeconomic models are designed to predict the chaotic system that is the economy. There is a broad range of methods designed to do this, ranging from the very simple to the extremely intricate. Most, with the advent of readily available supercomputers (eg your phone), will be able to be computed in a reasonable amount of time.

## Portfolio Balance Model

The Portfolio Balance Model (PBM) was the model employed by the MPC to estimate the effects of Large-Scale Asset Purcchase (LSAP) on inflation rate. The MPC had a target inflation rate of 2%$\c{1}$ which was not being met during the economic crash.$\c{2}$ Course notes by Michael Bergman$\c{3}$ from the University of Copenhagen (based on a 2002 textbook by Sarno and Taylor$\c{4}$) detail the portfolio balance model, which I will only summarise here. The model is based on modelling the demand for money, domestic bonds and foreign bonds (most composed of foreign currency). The model is based on equilibrium from the rates of change of these values, and thus predicts inflation based on this. The MPC used this to predict how many assets to buy, and used their high decision turnover rate to be able to finely tune how many assets to buy.

The model's underlying assumption is that the portfolio of a country's assets will tend towards a balance; the demand for the types of assets will reach a stable solution.

### Imperfect Arbitrage

The model used by the MPC takes into account imperfect arbitrage, so there were additional considerations for the existence of arbitrage, perhaps in the form of shocks (random, unexpected changes to the economic system such as from government scandals or extreme weather) or other new variables.

## Dynamic Stochastic General Equilibrium

The Macroeconomic Effects of Large-Scale Asset Purchase (MELP) is a 2011 paper published as a staff report from the Federal Reserve.$\c{5}$ It was released originally just after the Federal Reserve announced their QE2 program, a second wave of LSAP after the first didn't sufficiently stimulate the economy. The point of the paper was to prove that LSAP would have a meaningful impact on the economy, to try and counter the argument made in Wallace's 1981 paper$\c{6}$ that postulates that under certain conditions, central banks buying securities won't affect the economy.

The model is based on the interactions between 6 main factions of the economy:
* Households - the monopolistic suppliers of labour that consume, invest and pay taxes
* Labour Agencies - agents that combined differentiated labour into a composite
* Capital Producers - investers that manage their capital imperfectly and produce additional capital for their shareholders
* Intermediate Goods Producers - agents that produce intermediate goods from labour and capital
* Final Goods Producers - agents that combine differentiated intermediate goods into a homogenous good
* The Government - a single body that determines interest rate, implements LSAP and control long-term bonds

Each of these has their own technology that accounts for the others and attempts to maximise their profits. For example, a household will attempt to maximise the following function:

$$\mathbb{E}\_t\sum\_{s=0}^\infty(\beta\_j\zeta\_w)^s\left[\Xi\_{t+s}^{j,p}\tilde{W}\_t^j(i)L\_{t+s}^j(i)-\frac{\varphi\_{t+s}^j(L\_{t+s}^j(i))^{1+\nu}}{1+\nu}\right]$$

This frankly terrifying equation is part of the technical report$\F{1}$, which describes more thoroughly the mathematical aspects of the model. It ultimately says that you want to maximise your pay, but if your work has a greater supply of workers, then you will have to work for less.

### MELP Conclusions

The paper concludes, having run simulations of multiple LSAP programs, that "The effects of recent [2008] asset purchase programs on macroeconomic variables, such as GDP growth and inflation, are likely to be moderate but with a lasting impact on the level of GDP".$\c{5}$ However, the authors admit that the effects on GDP growth are unlikely to exceed 50bp. The authors suggest that keeping interest rates low for "some period of time" alongside this LSAP will cause the LSAP to be twice as effective.

---
# Footnotes

$\F{1}$ In appendix A, the technology of The Macroeconomic Effects of LSAP$\c{5}$

---
# Bibliography

$\c{1}$ “Quantitative Easing.” Accessed July 25, 2018. http://www.bankofengland.co.uk/monetary-policy/quantitative-easing.

$\c{2}$ “United Kingdom Inflation Rate in 2009.” Accessed July 27, 2018. https://www.statbureau.org/en/united-kingdom/inflation/2009.

$\c{3}$ Bergman, Michael. “The Portfolio Balance Model.” Institute of Economics, University of Copenhagen, March 16, 2005. https://www.hse.ru/data/2011/10/05/1270638325/Bergman%20%D1%81%D1%82%D0%B0%D1%82%D1%8C%D1%8F%20%D0%BF%D0%BE%20%D0%BF%D0%BE%D1%80%D1%82%D1%84.%20%D0%BC%D0%BE%D0%B4%D0%B5%D0%BB%D0%B8%20.pdf.

$\c{4}$ Sarno, Lucio, and Mark P. Taylor. The Economics of Exchange Rates. Cambridge, UK ; New York, NY: Cambridge University Press, 2002.

$\c{5}$ Chen, Han, Vasco Curdia, and Andrea Ferrero. “The Macroeconomic Effects of Large-Scale Asset Purchase Programs.” SSRN Electronic Journal, 2011. https://doi.org/10.2139/ssrn.1976319.

$\c{6}$ Wallace, Neil. "A Modigliani-Miller Theorem for Open-Market Operations." The American Economic Review 71, no. 3 (1981): 267-74. http://www.jstor.org/stable/1802777.
