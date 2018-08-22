---
Title: Marginal to Joint
Template: LeafPage
---
#Marginal Distributions to a Joint Distribution

A copula is a function that maps individual marginal distributions into a joint distribution. Li (2000) discusses how this is done: 

For a given univariate marginal distribution functions $F_1(x_1), ..., F_n(x_n)$ of random variables $X_1, ..., X_n$, it can be concluded that 
          	
		      $C_{\rho}(F_1(x_1), ..., F_n(x_n))$
          
	        $= Pr(F_1^{-1}(U_1) \leq x_1, ..., F_n^{-1}(U_n) \leq x_n)$
          
	        $= Pr(X_1 \leq x_1, ..., X_n \leq x_n)$
          
	        $= F(x_1, ..., x_n)$
          
Furthermore, for the marginal distribution functions of the $X_i$ you get:

          $C_{\rho}(F_1(\infty), ..., F_{i-1}(\infty), F_i(x_i), F_{i+1}(\infty), ..., F_n(\infty))$

          $=Pr(X_1 \leq \infty, ..., X_{i-1} \leq \infty, X_i \leq x_i, X_{i+1} \leq \infty, ..., X_n \leq \infty)$

          $= Pr(X_i \leq x_i)$

          $= F_i(x_i)$

##References

[1] David X. Li. On Default Correlation: A copula function approach. *Journal of Fixed Income,*: (4):43-54, April 2000.
