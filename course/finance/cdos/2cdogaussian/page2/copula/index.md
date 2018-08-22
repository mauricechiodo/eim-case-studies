---
Title: What is a Copula?
Template: LeafPage
---

#What is a Copula?

Copulas are an essential tool for understanding several problems about stochastic dependence (i.e. when the dependence between random variables can be expressed by a change of the conditional distribution of any of the variables when the other variables are altered) and can be applied to a variety of mathematical areas including probability, real analysis, measure theory, and algebraic structures.

Ultimately, an independence assumption of the credit risks is not realistic, as in reality, the default rate for a group of credits tends to be higher in a recession and lower when the economy is booming. 
So, each credit is subject to the same set of macroeconomic environmental factors and we can see that there exists some form of positive dependence among the credits. 
To introduce a correlation structure, we must determine how to specify a joint distribution given marginal distributions. 

A copula is a multivariate probability distribution function with uniform marginal distribution functions. Copulas allow us to separate the problem of estimating a multidimensional distribution of several variables into the estimation of:
	- the individual marginal distributions;
	- the joint dependency structure between these one-dimensional random variables. 

Click [here](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page2/copula/formal) for the formal definition.

Li (2000) describes [how copula functions can be used to link marginal distributions with a joint distribution](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page2/copula/marginaltojoint). 

In 1959, Sklar established a very important result: 

    Given an $n$-dimensional multivariate distribution function and the related marginal distribution functions, 
    
    there exists a copula that will map these individual marginal distributions into a joint distribution.

Click [here](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page2/copula/proof) for the proof of this result. 

We should emphasize that Sklar's theorem **only** ensures the exsistence of a copula, but the [appropriate choice of a copula function](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page2/modelappropriate.md) which matches the specific model requirements is fraught with risk. 

##References

[1] David X. Li. On Default Correlation: A copula function approach. *Journal of Fixed Income,*: (4):43-54, April 2000.

[2] A.V. Prokhorov. Stochastic dependence, 2011.

[3] Abe Sklar. Fonctions de Répartition à n Dimensions et Leurs Marges. *Publications de l'Institut Statistique de l'Université de Paris,*: 229-231, 1959.
