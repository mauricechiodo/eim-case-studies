---
Title: Formal Definition
Template: LeafPage
---

#Formal Defintion of a Copula

As stated in 'Princples of Copula Theory' (2015), the formal definition of a copula is:

Let U_1, ..., U_n be uniformly distributed random variables in [0,1]. 
	
A multivariate distribution function $C_{\rho}: [0,1]^n \rightarrow [0,1]$ with

	                 $C_{\rho}(u_1, u_2, ..., u_n) = Pr[U_1 \leq u_1, ..., U_n \leq u_n)$
                    
is called **Copula-function** provided the following conditions are met:

	1. $C_{\rho}(u_1, ..., u_n) = 0$ if $u_i = 0$ for at least one $i \in \{1, 2, .., n\}$
	2. $C_{\rho}(1, ..., 1, u_k, 1, ..., 1) = u_k$ for $k = 1, ..., n$.
	3. $C_p$ is non-decreasing. 
	
Note that $\rho$ is the general dependence parameter that characterizes the correlation structure of the copula. 

##References 

[1] Fabrizio Durante and Carlo Sempi. *Principles of Copula Theory.* CRC Press, 2015.
