---
Title: ZestFinance Patent
Template: LeafPage
---

#ZestFinance Patent

In January 2015, ZestFinance was granted a patent entitled 'System and method for building and validating a credit scoring function'. In the patent they give an overview of the method: 
	1. Raw datasets are generated using the borrower's profile from one or more of the following: borrower's data, proprietary data, public data, and social network data. For example, the raw datasets may include the following data: classical financial data of the borrower's profile (e.g. FICO score, current salary, length of most recent employment, number of bankruptcies), number of internet domains owned, organisations the borrower has been or currently is involved with, how many lawsuits the borrower has, the psychological characteristics based on his or her interests, and other non-traditional aspects of the borrower's identity and history.
	2. The raw datasets are transformed into variables in their most useful form. For example, a *current income* variable could be left in its original form or converted into a scale: 
		- $0$ = no income;
		- $1 =  \$ 1 - \$ 5,000$;
		- $2 = \$ 5,001 - \$ 20,000$, etc.
    
  If the application is submitted on the website, then browser-related behavioural measurements, such as the number of pages viewed by the applicant and the amount of time the applicant spent on the actual application pages, can also be used as numerical signals related to creditworthiness.
	3. Then the computer processes the variables using one or more algorithms to generate independent decision sets describing specific aspects of a borrower (meta-variables). Meta-variables are not only a measure of creditworthiness, but they can also be useful in constructing a credit-scoring function (the reasons why can be found on page 4-5 of the patent).  Statistical analysis of meta-variables are instructive as to which "signals" are to be measured and what weight is to be assigned to each. 
	>*"Indeed, constructing meta-variables may not be a fully automated process, but rather a heuristic one, calling for **expert** skill." So, only the expert can fully understand how this process is done. I want to emphasize that the expert they refer to here is a data scientist, i.e. a mathematician.*
	4. Next, the meta-variables are fed into statistical, financial, and other algorithms each with a different predictive "skill". 
	5. Finally, each of the models then "vote" their individual importance and then they're assembeled into a final score. There are many ways to perform this assembly of scores using machine learning or statistical algorithms. A simple example is shown in page 5 of the patent document [2]. 

![ZestFinance's modeling and scoring process](http://cueimps.soc.srcf.net/course/media/ZestFinance.png "ZestFinance's modeling and scoring process [5]")

Looking at the detailed description of the method, and as observed by Hardy in an article in the New York Times entitled 'Big Data for the Poor', we can see that the ZestFinance model also considers the spending habits in the context of a borrower's geographic location. 

For example, *"paying half of one's income [on rent] in an expensive city like San Francisco might be a sign of conventional spending, while paying the same amount in cheaper Fresno could indicate profligacy" (profligacy: reckless extravagance or wastefulness in the use of resources).*

**But, why should we care about this?** Click [here](http://cueimps.soc.srcf.net/course/course/credit-scores/Credit_Scores/zestfinance/patent/discussion).

##References

[1] Douglas C. Merrill, Shawn M. Budde, John W.L. Merrill, Lingyun Gu, and James P. McGuire. System and method for building and validating a credit scoring function, January 2015. 

[2] Quentin Hardy. Big Data for the Poor. *The New York Times,* July 2012. 
