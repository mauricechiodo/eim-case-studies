---
Title: Gaussian Copula Model
Template: LeafPage
---

In a typical CDO, if the correlation amongst the bonds or loans in the pool was low, only the holders of the lowest tranche would be at a great risk of losing some or all of their investment. 
However, if the correlation was very high, many of the bonds or loans might default and so the losses could impact even the most senior tranche. 
As a result, modeling correlation was the most crucial problem in CDO evaluation, and [Gaussian copulas](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page2/gaussiancopula.md) became the most popular way to do this due to David Li's paper, published in 2000, entitled 'On Default Correlation: A copula function approach'.

##Why the Gaussian Copula?

In "The Formula That Killed Wall Street’: The Gaussian Copula and Modelling Practices in Investment Banking' (2014), MacKezie discusses events that occured before Li's 2000 paper, which help us to see why the Gaussian Copula was chosen.

Before Li, Vasicek, a probability theorist, formulated an analytically-solvable special case: a pool of a large number of equally-sized loans, all due at the same time with the same probability of default and the same correlation between the values of the assets of any pair of borrowers (these features are why Vasicek’s special case is often called the ‘large homogeneous pool’ model). 
There was almost no direct empirical data to guide his modelling so he used the standard model of asset-value fluctuations - geometric Brownian motion - and the mathematically most familiar correlation structure - the multivariate Gaussian distribution.

However, both this work and CreditMetrics - J.P. Morgan’s 1997 software system to measure credit risk - were 'one-period’ models, meaning that although the underlying stochastic processes took place in continuous time, all that was modelled was *whether* corporations defaulted within a single given time period, and not *when* in that period they defaulted.

Employing his experience in acturial sciences, Li was able to overcome this limitation using Copula functions. Click [here](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page2/copula/copula.md) for more information on what a Copula Function is. 

Hence, although [other copula functions](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page2/othercopulas.md) were discussed by Li in his paper (and by others who were also exploring the applicability of copula functions to insurance and finance), this connection to CreditMetrics – already a well-established, widely-used model – together with the simplicity and familiarity of the Gaussian (and the ease of implementing it) meant that ultimately the [Gaussian Copula](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page2/gaussiancopula.md) was chosen.

We must consider whether these are good enough reasons for choosing the Gaussian distribution. 
It seems that some investigation into the behaviour of the market, along with a wider analysis of whether other Copulas were more appropriate should have been done. Click [here](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page2/modelappropriate.md) for more information. 

But, what happened after Li published his paper? Click [here](http://db716.user.srcf.net/eim/course/finance/cdos/2cdogaussian/page3/page3.md) to find out. 

##References

[1] David X. Li. On Default Correlation: A copula function approach. *Journal of Fixed Income,*: (4):43-54, April 2000.
[2] Donald MacKenzie and Taylor Spears. 'The Formula That Killed Wall Street': The Gaussian Copula and Modelling Practices in Investment Banking. *Social Studies of Science,* 44:393-417, 2014.
