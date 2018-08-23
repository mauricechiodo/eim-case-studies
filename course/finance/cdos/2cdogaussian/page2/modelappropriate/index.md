---
Title: Copula Models
Template: LeafPage
---

#Is the Copula Model Appropriate?

A large variety of models have been developed and some of their properties have been investigated. As discussed by Rüschendorf in 'Copulas, Sklar's Theorem, and Distributional Transform', the following questions are important to consider when deciding the how appropriate the Copula model is to the situation being modelled:

	- Is the range of dependence of these models wide and flexible enough?
	
	- Which of these models have tail dependence and are therefore able to model situations where there is strong positive dependence in tails?
	
	**What is Tail Dependence?** 
	
	Suppose we have two random variables X and Y. Tail dependence is the probability that Y reaches extremely large values, given that random variable X attains extremely large values.
	
	Say we have two mortgages A and B for houses on the same road and A defaults - a very unlikely event. Then, given this, the probability that B will default is greater than 0. Hence, to model mortgages, we need a copula model with tail dependence. But, the Gaussian Copula does not, which was one of the major limitations for applying it to this context [(click here for more information)](http://cueimps.soc.srcf.net/course/course/finance/cdos/cdoeffectsdylan).
	
- Is there some parameter that can describe the degree of dependence?

- Is there some natural probabilistic interpretation of the model describing certain situations?

- Is there a closed form of the copula or a simple simulation algorithm that can be applied? 

	
##References

[1] Ludger Rüschendorf. Copulas, Sklar's Theorem, and Distributional Transform. In *Mathematical Risk Analysis*, pages 3-34. Springer, Berlin, Heidelberg, 2013.
