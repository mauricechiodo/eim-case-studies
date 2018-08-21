---
Title: Copula Theory
Template: LeafPage
---

#Copula Theory

An independence assumption of the credit risks is not realistic. In reality, the default rate for a group of credits tends to be higher in a recession and lower when the economy is booming. So, each credit is subject to the same set of macroeconomic environmental factors and we can see that there exists some form of positive dependence among the credits. To introduce a correlation structure, we must determine how to specify a joint distribution given marginal distributions. 

A copula is a multivariate probability distribution function with uniform marginal distribution functions. Copulas allow us to separate the problem of estimating a multidimensional distribution of several variables into the estimation of:
  * the individual marginal distributions;
	* the joint dependency structure between these one-dimensional random variables. 
Put simply, a copula is a function that maps individual marginal distributions into a joint distribution.

As stated in 'Princples of Copula Theory' (2015) 13, the formal definition of a copula is:

	Let U_1, ..., U_n be uniformly distributed random variables in [0,1]. 
	
	A multivariate distribution function $C_{\rho}: [0,1]^n \rightarrow [0,1]$ with

	                 $C_{\rho}(u_1, u_2, ..., u_n) = Pr[U_1 \leq u_1, ..., U_n \leq u_n)$
                    
is called **Copula-function** provided the following conditions are met:
	1. $C_{\rho}(u_1, ..., u_n) = 0$ if $u_i = 0$ for at least one $i \in \{1, 2, .., n\}$
	2. $C_{\rho}(1, ..., 1, u_k, 1, ..., 1) = u_k$ for $k = 1, ..., n$.
	3. $C_p$ is non-decreasing. 
	
Note that $\rho$ is the general dependence parameter that characterizes the correlation structure of the copula. 

Li (2000) 9 highlights how copula functions can be used to link marginal distributions with a joint distribution: for a given univariate marginal distribution functions $F_1(x_1), ..., F_n(x_n)$ of random variables $X_1, ..., X_n$, it can be concluded that 
          	
		$C_{\rho}(F_1(x_1), ..., F_n(x_n))$
          
	        $= Pr(F_1^{-1}(U_1) \leq x_1, ..., F_n^{-1}(U_n) \leq x_n)$
          
	        $= Pr(X_1 \leq x_1, ..., X_n \leq x_n)$
          
	        $= F(x_1, ..., x_n)$
          
Furthermore, for the marginal distribution functions of the $X_i$ you get:

          $C_{\rho}(F_1(\infty), ..., F_{i-1}(\infty), F_i(x_i), F_{i+1}(\infty), ..., F_n(\infty))$

          $=Pr(X_1 \leq \infty, ..., X_{i-1} \leq \infty, X_i \leq x_i, X_{i+1} \leq \infty, ..., X_n \leq \infty)$

          $= Pr(X_i \leq x_i)$

          $= F_i(x_i)$

Copulas are an essential tool for understanding several problems about stochastic dependence (i.e. when the dependence between random variables can be expressed by a change of the conditional distribution of any of the variables when the other variables are altered 21) and can be applied to a variety of mathematical areas including probability, real analysis, measure theory, and algebraic structures.

##Sklar's Theorem

In 'Fonctions de Répartition à n dimensions et leurs marges' (1959) 25, Sklar established the converse:

	Let $F$ be a multivariate $n$-dimensional distribution function and $F_1, ..., F_n$, the related marginal distribution functions. 
	
	Then there exists an $n$-dimensional Copula $C_{\rho}$, so that the following equation holds for all $(x_1, ..., x_n) \in \mathbb{R}^n$:	
	
	$F(x_1, ..., x_n) = C_{\rho}(F_1(x_1), ..., F_n(x_n))$

The rest of this section and the following section is based on ideas from chapter 1 of 'Mathematical Risk Analysis' (2013) entitled 'Copulas, Sklar’s Theorem, and Distributional Transform' 17.

Before proving the result we first define a **distributional transform**:

Let Y be a real random variable with distribution function F and let $V$ be a random variable independent of $Y$, such that $V \sim U(0,1)$. The modified distribution function $F(x, \lambda)$ is defined by 

	        $F(x, \lambda) := P(X < x) + \lambda P(Y = x)$

We call $U := F(Y, V)$ the **distributional transform** of Y. 

**Proposition:**

	Let U  = F(Y,V) be the distributional transform of Y. 
	
	Then $U := U(0,1)$ and $Y = F^{-1}(U)$ almost surely.

Note that in probability theory, we say that an event happens almost surely if it happens with probability one.

**Proof of Sklar's Theorem:**

	Let $X$ = ($X_1, ..., X_n$) be a random vector on a probability space ($\Omega$, $\mathcal{F}$, P), with distribution function F and let $V \sim U(0,1)$ be independent of X. 
	
	Considering the distributional transforms $U_i := F_i(X_i, V), 1 \leq i \leq n$, we have by the proposition above that $U_i := U(0,1)$ and $X_i = F_i^{-1}(U_i)$ almost surely, $1 \leq i \leq n$. 

	Thus defining C to be the distribution function of $U = (U_1, ..., U_n)$ we obtain

          	$F(x) = P(X \leq x) = P(F_i^{-1}(U_i) \leq x_i, 1 \leq i \leq n)$

          	$= P(U_i \leq F_i(x_i), 1 \leq i \leq n) = C(F_1(x_1),..., F_n(x_n))$

	i.e. C is the copula of F. 

We should emphasize that Sklar's theorem **only** ensures the exsistence of a copula, but the appropriate choice of a copula function which matches the specific model requirements is fraught with risk. There are a variety of copula functions used in practice which can model different dependence structures.  
