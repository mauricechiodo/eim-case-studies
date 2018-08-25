---
Title: Empirical Analysis
Template: ListSubPages
---

# Empirical Analysis
$\newcommand{\F}[1]{^{[\text{F}#1]}}$$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$$\newcommand{\c}[1]{^{[#1]}}$$\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$
The model is estimated with Bayesian methods 6 The likelyhood is constructed using the ‘Kalman filter’, based on the state space representation of the rational expectations solution of the model.

## [Data](/course/course/finance/quantitative-easing/modelling/technical-appendix/empirical-analysis/data)

Quarterly data from the United States from 1987 to 2009 is used for

1. Real GDP per capita
2. Hours worked
3. Real wages
4. Core personal consumption expenditures deflator
5. Nominal effective Federal funds rate
6. 10-year Treasury constant maturity yield

All data were extracted from the Federal Reserve Economic Data, data which is maintained by the Federal Reserve Bank of St. Louis. The equations related to these data are as follows

$$\Delta Y\_t^{obs}=100\left(\gamma+\hat{Y}\_{z,t}-\hat{Y}\_{z,t-1}+\hat{z}\_t\right)$$
$$L\_t^{obs}=100\left(L+\hat{L}\_t\right)$$
$$\Delta w\_t^{obs}=100\left(\gamma+\hat{w}\_{z,t}-\hat{w}\_{z,t-1}+\hat{z}\_t\right)$$
$$\pi\_t^{obs}=100\left(\pi+\hat{\pi}\_t\right)$$
$$r\_t^{obs}=100\left(r+\hat{r}\_t\right)$$
$$r\_{L,t}^{obs}=100\left(r\_{L,t}+\hat{r}\_{L,t}\right)$$

Here $\pi\equiv\ln\left(\Pi\right)$, $r\equiv\ln\left(R\right)$ and $r\_L\equiv\ln\left(R\_L\right)$.

The authors decided a prior distribution for the variables and used experimental results to create a posterior distribution. The stability of their data is tested by using data ending not only in 2009q3, but also 2007q2, 2008q3 and 2011q2. The parameters remained comparable throughout the data changes.

## Prior Choice

In MELP the authors summarize the prior choices of each distribution.$\Ci{1}{Tables 2-3} For all variables, the distribution depends on its domain or if it is a shock innovation.

* Gamma distribution (‘G’) for parameters $X$ such that $X\in[0,\infty]$
* Beta distribution (‘B’) for parameters $X$ such that $X\in[0,1]$
* Inverse-Gamma (‘IG1’) for shock innovations. IG1 has a domain of $[0, \infty]$

## [Posterior Distribution](/course/course/finance/quantitative-easing/modelling/technical-appendix/empirical-analysis/posterior-distribution)

The posterior distributions were generated using the ‘Metropolis random walk Markov Chain Monte Carlo’ (MCMC) simulation method$\C{1}{23}$, which from what I can gather this is hundreds of thousands of samples. The results emerges that the market segmentation is very small, with $\omega\_u\in(0.72,0.99)$ approximately, with a median of 0.934 and a mode of 0.987. Since the data ends in 2009q3, the authors check the stability of this estimate by considering alternative endings, having the last data be from 2007q2$\F{2}$ , 2008q3$\F{3}$ and 20011q2.$\F{4}$ The parameters remained comparable throughout these data changes.

The other key parameter, according to the authors, is the elasticity of the risk premium to asset purchases $\zeta'$ . If the elasticity was 0, asset purchases wouldn’t affect risk premium or real economy. The prior and posterior distributions for this are very similar, suggesting the data do not affect $\zeta'$ very much.

---

---

# Footnotes

$\F{1}$ For shock innovations only

$\F{2}$ Before the financial turbulence

$\F{3}$ Before the ZLB was hit

$\F{4}$ Most recent data at time of authors writing

---

# Bibliography

$\c{1}$ Han Chen, Vasco Curdia and Andrea Ferrero. “The Macroeconomic Effects of Large-Scale Asset Purchase Programs”. en. In: SSRN Electronic Journal (2011). issn: 1556-5068. doi: 10.2139/ssrn.1976319. url: http://www.ssrn.com/abstract=1976319 (visited on 2018-07-19).
