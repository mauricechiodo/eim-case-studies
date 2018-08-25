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
$$\Delta w\_t^{obs}=100(\gamma+\hat{w}\_{z,t}-\hat{w}\_{z,t-1}+\hat{z}\_t)$$
$$\pi_t^{obs}&=100(\pi+\hat{\pi}\_t)$$
$$r\_t^{obs}=100(r+\hat{r}\_t)$$
$$r\_{L,t}^{obs}&=100(r\_{L,t}+\hat{r}\_{L,t})$$

Here $\pi\equiv\ln\left(\Pi\right)$, $r\equiv\ln\left(R\right)$ and $r\_L\equiv\ln\left(R\_L\right)$.

The authors decided a prior distribution for the variables and used experimental results to create a posterior distribution. The stability of their data is tested by using data ending not only in 2009q3, but also 2007q2, 2008q3 and 2011q2. The parameters remained comparable throughout the data changes.

## [Posterior Distribution](/course/course/finance/quantitative-easing/modelling/technical-appendix/empirical-analysis/posterior-distribution)

## Prior Choice

The random variables, $X$, were given the distribution of either gamma ($X\in[0,\infty]$), beta ($X\in[0,1]$) or inverse-gamma$\F{1}$ ($X\in[0,1]$).

---

---

# Footnotes

$\F{1}$ For shock innovations only
