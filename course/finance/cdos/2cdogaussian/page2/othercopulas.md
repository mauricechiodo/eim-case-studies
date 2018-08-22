---
Title: Other Copulas
Template: LeafPage
---

#Other Copulas

There are a variety of different classes of copulas. The ones presented below have been taken from chapter 1 of 'Mathematical Risk Analysis' by Rüschendorf (2013) and others were discussed by Li (2000) before he ultimately choose to use the Gaussian copula.

##Farlie--Gumbel--Morfenstern (FGM) Copula

The Farlie--Gumbel--Morfenstern (FGM) Copula is:

      $C_\alpha(u,v) = uv(1 + \alpha(1-u)(1-v)), |\alpha| \leq 1$

There are also its generalised versions - EFGM copulas, which are extensions of FGM to the $n$-dimensional case. They're given by:

      $C(u) = \prod_{i=1}^nu_i(1 + \sum_{T \subset \{1,..., n\}}\alpha_T\prod_{j \in T}(1-u_j))$ 

      for suitable $\alpha_T \in \mathbb{R}^1.$

Some examples of applications of this family of copulas is discussed by Lai and Balakrishnan in 'Distributions Expressed as Copulas': 
  - fitting data on the joint occurrence of certain trace elements in water;
	- a starting point when considering how a population probability distribution function is altered in the surviving and nonsurviving groups by a risk function;
	- reanalysing datasets on the effects of mixtures of poisons.

##Archimedean Copulas

Archimedean Copulas are of the following form:

      $C_{\Phi}(u_1,...,u_n) = \Phi^{-1}(\Phi(u_1) + ... + \Phi(u_n))$

      for some generator $\Phi: (0,1] \rightarrow \mathbb{R}_+)$ with $\Phi(1) = 0$, 
      
      such that $\Phi$ is completely monotone. 

When $\Phi(t) = \frac{1}{\alpha}(t^{-\alpha} - 1)$ we get the **Clayton copula**:

      $C_\alpha(u) = (\sum u_i^{-\alpha}-n+1)^{-\frac{1}{\alpha}}, \alpha > 0$

When $\Phi_\delta(t) = -\frac{1}{\delta}\log(1 - (1-e^{-\delta})e^{-t})$ we get the **Frank copula**:

      $C_\delta(u) = -\frac{1}{\delta}\log(1 + \frac{\prod_{i = 1}^n(e^{-\delta u_i}-1)}{(e^{-\delta}-1)^{n-1}})$

Archimedean copulas are popular in practivce as they allow modeling dependence in arbitrarily high dimensions with only one parameter that determines the strength of dependence.

##Bivariate Normal

The formula for the Bivariate Normal Copula is 

      $C(u,v) = \Phi_2(\Phi^{-1}(u), \Phi^{-1}(v), \rho), -1 \leq \rho \leq 1$

      where $\Phi_2$ is the bivariate normal distribution function with correlation coefficient $\rho$, 
      
      and $\Phi^{-1}$ is the inverse of a univariate normal distribution function. 

##Bivaraite Mixture Copula Function

We can form a new copula function using existing copulas. 

If two uniform random vairable $u$ and $v$ are independent, we have a copula function $C(u,v) = uv$. 

If two random variables are perfectly correlated we have the copula function $C(u, v) = \min(u,v)$. 

Mixing the two copula functions above by a mixing coefficient ($\rho > 0$) we obtain a new copula function as follows:
    - $C(u,v) = (1 - \rho)uv + \rho \min(u,v)$, if $\rho > 0$. 
    - $C(u,v) = (1+\rho)uv - \rho(u - 1 + v)\Theta(u - 1 +v)$, if $\rho \leq 0$
      where $\Theta(x) = 1$, if $x \geq 0$ and $\Theta(x)= 0$, if $x < 0$

##References

[1] Chin Diew Lai and N. Balakrishnan. Distributions Expressed as Copulas. In *Continuous Bivariate Distributions*, pages 67-103. Springer, 2009. 

[2] David X. Li. On Default Correlation: A copula function approach. *Journal of Fixed Income,*: (4):43-54, April 2000.

[3] Ludger Rüschendorf. Copulas, Sklar's Theorem, and Distributional Transform. In *Mathematical Risk Analysis*, pages 3-34. Springer, Berlin, Heidelberg, 2013.
