---
Title: Gaussian Copula Page (Maria)
Template: LeafPage
---

#Pricing CDOs

*"[Li's Model] was a very simple mathematical answer almost anyone could use... and when you've got a hammer, everthing suddenly looks like a nail."* -Professor Harry Pajer (Li's Mentor at the University of Waterloo)

[Insert Video Here]

In the late 1990s banks became interested in looking for new ways to increase returns whilst diversifying their own risks. As a result, a new type of financial product emerged: Multi-name Credit Derivatives. These appeared to be a perfect way to achieve this goal. The most popular of these multi-name credit derivatived were the Collateralised Debt Obligations (CDOs), which are structured asset-back securities. 

The high profitablitiy for the issuers of these products and the fact that their structure allowed banks to spread their own credit risk made them very attractive and generated a lot of interest from financial institutions. The questioned remained: **Was there an efficient way to price these credit derivatives?**

In a typical CDO, if the correlation amongst the  bonds or loans in the pool was low, only the holders of the lowest tranche would be at a great risk of losing some or all of their investment. However, if the correlation was very high, many of the bonds or loans might default and so the losses could impact even the most senior tranche. As a result, modelling correlation was the most crucial problem in CDO evaluation, and Gaussian copulas became the most popular way to do this due to David Li's paper, published in 2000, entitled 'On Default Correlation: A copula function approach'.

Before Li, Vasicek, a probability theorist, formulated an analytically-solvable special case: a pool of a large number of equally-sized loans, all due at the same time with the same probability of default and the same correlation between the values of the assets of any pair of borrowers (these features are why Vasicek’s special case is often called the ‘large homogeneous pool’ model). There was almost no direct empirical data to guide his modelling so he used the standard model of asset-value fluctuations - geometric Brownian motion - and the mathematically most familiar correlation structure - the multivariate Gaussian distribution.

However, both this work and CreditMetrics - J.P. Morgan’s 1997 software system to measure credit risk - were 'one-period’ models, meaning that although the underlying stochastic processes took place in continuous time, all that was modelled was *whether* corporations defaulted within a single given time period, and not *when* in that period they defaulted.

Employing his experience in acturial sciences, Li was able to overcome this limitation using Copula functions. 

Hence, although other copula functions were discussed by Li in his paper (and by others who were also exploring the applicability of copula functions to insurance and finance), this connection to CreditMetrics – already a well-established, widely-used model – together with the simplicity and familiarity of the Gaussian (and the ease of implementing it using, for example, Monte Carlo Simulations) meant that ultimately the Gaussian Copula was chosen. 

You may be asking, **what is a copula?**

Ultimately, an independence assumption of the credit risks is not realistic, as in reality, the default rate for a group of credits tends to be higher in a recession and lower when the economy is booming. So, each credit is subject to the same set of macroeconomic environmental factors and we can see that there exists some form of positive dependence among the credits. To introduce a correlation structure, we must determine how to specify a joint distribution given marginal distributions. 

A copula is a multivariate probability distribution function with uniform marginal distribution functions. Copulas allow us to separate the problem of estimating a multidimensional distribution of several variables into the estimation of:
	- the individual marginal distributions;
	- the joint dependency structure between these one-dimensional random variables. 

In 1959, Sklar established a very important result: given an $n$-dimensional multivariate distribution function and the related marginal distribution functions, there exists a copula that will map these individual marginal distributions into a joint distribution.

We should emphasize that Sklar's theorem **only** ensures the exsistence of a copula, but the appropriate choice of a copula function which matches the specific model requirements is fraught with risk. There are a variety of copula functions used in practice which can model different dependence structures.  As detailed above, ultimately the Gaussian Copula was chosen. However, we must consider whether the reasons why this distribution was chosen were good enough. Perhaps some investigation into the behaviour of the market, along with a wider analysis of whether other Copulas were more appropriate should have been done. 


The reaction of investment bankers to Li's model was electric. As Scott Patterson describes in his book 'The Quants': *The Gaussian copula was, in hindsight, a disaster. The simplicity of the model hypnotized traders into thinking that it was a reflection of reality.”*

Li made one big simplification in his model. He didn't just drastically decrease the difficulty of calculating correlations, he decided not to calculate all the relationships between the various loans that made up the underlying pool. In Li's model, the only thing that mattered was the final correlation number.

A recent discussion with a trader revelead that, to do their job, traders "choose the easiest model that works". However, as can be seen by the financial crisis of 2007/2008, this model clearly did not work.

[Link to Longer Summary Document]
