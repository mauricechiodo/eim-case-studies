---
Title: Gaussian Copula
Template: LeafPage
---

#Gaussian Copula

The Gaussian Copula uses Gaussian random variables instead of uniform random variables.

As presented in Li's 2000 paper, letting 

	$\Phi$ be the distribution function of the one-dimensional standard normal distribution and 
	$\Phi_{\Sigma}^{n}$ the distribution function of the $n$-dimensional standard normal distribution with positive definite correlation matrix $\Sigma$, 
	the $n$-dimensional Gaussian copula $C_{\Sigma}^{\Phi}$ can be defined as:

		$C_\Sigma^\Phi(u_1, ..., u_n) = \Phi_\Sigma^n(\Phi^{-1}(u_1), ..., \Phi^{-1}(u_n))$
		
		for all $(u_1, ..., u_n) \in [0,1]^n$. 

Considering the simplest case where $n = 2$, we obtain:

	$C_{p_{12}}^\Phi(u_1,u_2) = \int_{-\infty}^{\Phi^{-1}(u_1)} \int_{-\infty}^{\Phi^{-1}(u_2)}\frac{1}{2\pi(1-\rho^2_{12})^{\frac{1}{2}}}\exp[-\frac{s^2 - 2\rho_{12}*s*t + t^2}{2(1-\rho^2_{12})}]dsdt$

	with $(u_1, u_2) \in [0,1]^2$ 
	
	and $\rho_{12}$ being the correlation coefficient of the bivariate standard normal distribution.
  
##References

[1] David X. Li. On Default Correlation: A copula function approach. *Journal of Fixed Income,*: (4):43-54, April 2000.
