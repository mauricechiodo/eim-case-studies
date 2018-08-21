---
Title: Copula Models
Template: LeafPage
---

#Copula Models

Using Sklar's theorem we see that to construct a distributional model for a random vector X, it is sufficient to specify a copula model fitting to the data. 

A large variety of models have been developed and some of their properties have been investigated. The following questions are important to consider when deciding the how appropriate the Copula model is to the situation being modelled [2]:
	- Is the range of dependence of these models wide and flexible enough?
	- Which of these models have tail dependence and are therefore able to model situations where there is strong positive dependence in tails?
	
	**What is Tail Dependence?** 
	
	Suppose we have two random variables X and Y. Tail dependence is the probability that Y reaches extremely large values, given that random variable X attains extremely large values.
	
	Say we have two mortgages A and B for houses on the same road and A defaults - a very unlikely event. Then, given this, the probability that B will default is greater than 0. Hence, to model mortgages, we need a copula model with tail dependence. But, the Gaussian Copula does not, which was one of the major limitations for applying it to this context [(click here for more information)](http://db716.user.srcf.net/eim/course/finance/cdos/cdoeffectsdylan).
	
- Is there some parameter that can describe the degree of dependence?
- Is there some natural probabilistic interpretation of the model describing certain situations?
- Is there a closed form of the copula or a simple simulation algorithm that can be applied? 

#Gaussian Copula Function

Leading up to the financial crisis, the Gaussian copula function was the most widely used model in pricing multi-name credit structures, such as CDOs, due to Li's model approach presented in his 2000 paper 'On Default Correlation: A copula function approach' [1].

The Gaussian Copula uses Gaussian random variables instead of uniform random variables.

As presented in Li's paper [1], letting 

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

[2] Ludger Rüschendorf. Copulas, Sklar's Theorem, and Distributional Transform. In *Mathematical Risk Analysis*, pages 3-34. Springer, Berlin, Heidelberg, 2013.
