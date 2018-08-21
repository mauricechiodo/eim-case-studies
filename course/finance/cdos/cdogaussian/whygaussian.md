---
Title: Why the Gaussian Copula?
Template: LeafPage
---

#Why the Gaussian Copula?

In ``The Formula That Killed Wall Street’: The Gaussian Copula and Modelling Practices in Investment Banking' (2014) \cite{donald_mackenzie_formula_2014}, MacKezie discusses events that occured before Li's 2000 paper \cite{david_x._li_default_2000}, which help us to see why the Gaussian Copula was chosen. 

Previous to Li, Vasicek (a probability theorist) formulated an analytically-solvable special case: a pool of a large number of equally-sized loans, all due at the same time with the same probability of default and the same correlation between the values of the assets of any pair of borrowers (these features are why Vasicek’s special case is often called the ‘large homogeneous pool’ model). 

There was almost no direct empirical data to guide his modelling so he used the standard model of asset-value fluctuations - geometric Brownian motion - and the mathematically most familiar correlation structure - the multivariate Gaussian distribution.

However, both this work and CreditMetrics were `one-period’ models, which meant that although the underlying stochastic processes took place in continuous time, all that was modelled was \textit{whether} corporations defaulted within a single given time period, and not \textit{when} in that period they defaulted.

Employing his experience in acturial sciences, Li was able to overcome this limitation using Copula functions. 

Hence, although other copula functions were discussed by Li in his paper \cite{david_x._li_default_2000} (and by others who were also exploring the applicability of copula functions to insurance and finance), this connection to CreditMetrics – already a well-established, widely-used model – together with the simplicity and familiarity of the Gaussian (and the ease of implementing it) meant that ultimately the Gaussian Copula was chosen. 

We must consider whether these are good enough reasons for choosing the Gaussian distribution. It seems that some investigation into the behaviour of the market, along with a wider analysis of whether other Copulas were more appropriate should have been done. 
