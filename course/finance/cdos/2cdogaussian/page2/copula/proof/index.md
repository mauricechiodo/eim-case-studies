---
Title: Proof of Sklar's Theorem
Template: LeafPage
---

#Sklar's Theorem

Before proving the result we first define a **distributional transform**:

    Let Y be a real random variable with distribution function F 
    
    and let $V$ be a random variable independent of $Y$, such that $V \sim U(0,1)$. 
    
    The modified distribution function $F(x, \lambda)$ is defined by 

	        $F(x, \lambda) := P(X < x) + \lambda P(Y = x)$

    We call $U := F(Y, V)$ the **distributional transform** of Y. 

For continuous distribution functions $F$ , $F(x, \lambda)$ for all $\lambda$, and $U = F(Y)$ has distribution U(0,1).

##Proposition

Let U  = F(Y,V) be the distributional transform of Y. Then $U := U(0,1)$ and $Y = F^{-1}(U)$ almost surely.

Note that in probability theory, we say that an event happens almost surely if it happens with probability 1.

##Proof of Sklar's Theorem

Let $X$ = ($X_1, ..., X_n$) be a random vector on a probability space ($\Omega$, $\mathcal{F}$, P), with distribution function F and let $V \sim U(0,1)$ be independent of X. 
	
Considering the distributional transforms $U_i := F_i(X_i, V), 1 \leq i \leq n$, we have by the proposition above that $U_i := U(0,1)$ and $X_i = F_i^{-1}(U_i)$ almost surely, $1 \leq i \leq n$. 

Thus defining C to be the distribution function of $U = (U_1, ..., U_n)$ we obtain

          	$F(x) = P(X \leq x) = P(F_i^{-1}(U_i) \leq x_i, 1 \leq i \leq n)$

          	$= P(U_i \leq F_i(x_i), 1 \leq i \leq n) = C(F_1(x_1),..., F_n(x_n))$

i.e. C is the copula of F. 
