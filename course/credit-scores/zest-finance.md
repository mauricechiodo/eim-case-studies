---
Title: ZestFinance
Template: LeafPage
---

#Zest Finance

ZestFinance  has an *"all data is credit data"* [10] approach that combines conventional credit information with thousands of data points collected from consumers' offline and online activities. 

##Patent
In January 2015, ZestFinance was granted a patent entitled 'System and method for building and validating a credit scoring function' [2]. In the patent they give an overview of the method: 
	1. Raw datasets are generated using the borrower's profile from one or more of the following: borrower's data, proprietary data, public data, and social network data. For example, the raw datasets may include the following data: classical financial data of the borrower's profile (e.g. FICO score, current salary, length of most recent employment, number of bankruptcies), number of internet domains owned, organisations the borrower has been or currently is involved with, how many lawsuits the borrower has, the psychological characteristics based on his or her interests, and other non-traditional aspects of the borrower's identity and history.
	2. The raw datasets are transformed into variables in their most useful form. For example, a \textit{current income} variable could be left in its original form or converted into a scale: 
		- 0 = no income;
		- 1 = /$ 1 to /$ 5,000;
		- 2 = /$ 5,001 to /$ 20,000, etc.
    If the application is submitted on the website, then browser-related behavioural measurements, such as the number of pages viewed by the applicant and the amount of time the applicant spent on the actual application pages, can also be used as numerical signals related to creditworthiness.
	3. Then the computer processes the variables using one or more algorithms to generate independent decision sets describing specific aspects of a borrower (meta-variables). Meta-variables are not only a measure of creditworthiness, but they can also be useful in constructing a credit-scoring function (the reasons why can be found on page 4-5 of the patent [2].  Statistical analysis of meta-variables are instructive as to which "signals" are to be measured and what weight is to be assigned to each. 
	>*"Indeed, constructing meta-variables may not be a fully automated process, but rather a heuristic one, calling for \textbf{expert} skill." So, only the expert can fully understand how this process is done. I want to emphasize that the expert they refer to here is a data scientist, i.e. a mathematician.*
	4. Next, the meta-variables are fed into statistical, financial, and other algorithms each with a different predictive "skill". 
	5. Finally, each of the models then "vote" their individual importance and then they're assembeled into a final score. There are many ways to perform this assembly of scores using machine learning or statistical algorithms. A simple example is shown in page 5 of the patent document [2]. 

![ZestFinance's modeling and scoring processh](http://db716.user.srcf.net/eim/media/ZestFinance.jpg "ZestFinance's modeling and scoring process [5]")

Looking at the detailed description of the method, and as observed by Hardy in an article in the New York Times entitled 'Big Data for the Poor' [9], we can see that the ZestFinance model also considers the spending habits in the context of a borrower's geographic location. For example, *"paying half of one's income [on rent] in an expensive city like San Francisco might be a sign of conventional spending, while paying the same amount in cheaper Fresno could indicate profligacy" (profligacy: reckless extravagance or wastefulness in the use of resources).*

##Discussion

**Defining the problem and specifying the target variable:**

In order to use machine-learning techniques to solve a problem or make predictions, the data scientist must define the problem and decide exactly what they want to predict. In the case of an unstructured problem like predicting creditworthiness, where there's no single correct answer, "articulating a proper and quantifiable definition is critical" [5]. One way in which this can be done is by choosing a state or outcome of interest, referred to as a 'target variable'. Hurley and Adebayo highlight that:

>*A poorly-crafted definition could also lead to inadvertent discrimination, where "data miners [] unintentionally parse the problem and define target variables in such a way that protected classes happen to be subject to systematically less favorable determinations."*


Furthermore, when target variables are defined subjectively, there is a "grey area" in which human judgment may have resulted in bias, and there is no guarantee that the machine-learning process will necessarily correct this.

ZestFinance's patent application [2] does not give a definition of 'creditworthiness' or describe the target variable it uses and so it is unclear how they do this. 

Hurley and Adebayo also state that "there is also no reason to assume that these companies have the borrowers' interests at heart." 

>*"A recent study of online payday lending notes that the ``lenders [using] sophisticated technology and advanced algorithms to predict which applicants are most likely to repay loans ... continue to charge interest rates usually in excess of 300 percent APR...""* [5]

This may hint at the fact that alternative credit scorers, like ZestFinance, may not be truly interested in predicting consumer creditworthiness, but instead in finding vulnerable, high-value targets for payday loans (a relatively small amount of money lent at a high rate of interest on the agreement that it will be repaid when the borrower receives their next wages). Furthermore, the majority of payday borrowers come from poor and minority communities [11]. Therefore, rather than expanding access to underserved groups, these alternative credit scores may actually disservice historically disadvantaged groups.

**Gathering and tranforming data:**

For these alternative credit scoring models, big data is needed. In 'Big Data, a Big Disappointment for Scoring Consumer Creditworthiness' [8], Yu, McLaughlin and Levy describe the methods used to collect data.
	1. **Cookie:** a cookie can contain various types of information, including but not limited to, the time of visit, the subpages visited, the items purchased (if the data is being collected from an online retail website such as Amazon). Cookies can also designate a unique ID to someone's computer, which allows third party tracking companies to see other pages visited. 
	2. **Web Beacon:** this can not only track which webpages a person visits, but also records the text typed in. 
	3. **Web Crawling:** this involves the duplication and categorization of information from websites; programmers can write software that scans websites and sorts posts. 
 
 In relation to ZestFinance's credit scoring model, they collect the following data:
 	- the borrower's data: *information provided directly by the applicant during the application process, as well as other information such as web-browser activity, taken from the applicant's device at the time they applies for a loan online (e.g. how long the applicant spends reviewing the terms and conditions page to determine whether they read it carefully - used as a proxy for responsibility)*;
 	- proprietary data: *information obtained from privately or governmentally owned data stores and may encompass everything from an someone's online and offline purchase history to health and medical data*;
 	- public data: *information that ZestFinance obtains from automated searches of the Internet and techniques such as web crawling and scraping*;
 	- social network data: *information obtained from the borrower's social media posts and "any social graph information for any or all members of the borrower's social network"* [2].
 
This raw input data is not all necessarily objective, and may reflect forms of preexisting bias and discrimination. This is because not all data is created or collected equally. For example, there may be mechanisms that collect data that favours particular groups and excludes others. If the credit scores rely on non-neutral data collection methods, then the data may fail to give a representative sample of all groups and lead some groups being treated less favourably or ignored by the scorer's model. 
 
Another problem faced is accuracy. Whilst big data does address flaws in the current credit scoring system, there are definite drawbacks to expanding credit variables from 15 to thousands 30. Instead of minimising the impact of unimportant credit signal, a big data approach could amplify the significance of a completely irrelevant signal. 
 
 Nassim Taleb, a risk engineering professor at New York Univeristy, explains:
 
>*"…if I generate…a set of 200 variables — completely random and totally unrelated to each other—with about 1,000 data points for each, then it would be near impossible not to find in it a certain number of ‘significant’ correlations of sorts.”* [6]

Finally, data collection and transformation could lead to an issue of transparancy. Most, if not all, credit scoring companies treat their data sources as proprietary trade secrets. This means that, in practice, some consumers have no real means to understand what could potentially affect their credit ratings, and even less ability to challenge their scores, or test whether it is accurate. 

>*"Assuming that a diligent applicant could first identify an error among the thousands of entries in the credit scorer's raw data set, it is unlikely that the applicant would have the capacity to prove that the error resulted in a faulty score."* [5]

Furthermore, due to the extensive transformation process, which involves many aggregations and combinations of data points, as well as subjective decisions made by the data scientist, it is unlikely that a consumer could actually challenge their credit score. 

**Developing a final model through analysis of training data and feature selection:**

Not all inputs will be relevant. In fact, many are likely to be discarded as the system learns what is relevant to the target variable and what isn't. As can be gleaned from the ZestFinance patent [2], their feature selection process is not uniformly automated and the company selects the most relevant meta-variables in one of two ways:
	1. a data analyst curates, or manually determines, which meta-variables are significant, drawing from past experiences and observations of the applicant pool. 
	2. statistical algorithms are used to automatically identify the most significant metavariables. 

As a result, it isn't possible to see which of ZestFinance's metavariables have come out as the most significant, how they are calculated, or whether they accurately reflect creditworthiness. 

Additionally, the way in which the data scientist develops and refines the final credit-scoring model can cause issues with transparency and the abiltiy for a consumer to challenge scores. This is because the process is so complex it would be very hard to understand and determine if inaccuracies in the data have negatively influenced their score. 

The machine-learning and feature selection process may also result in models that have some bias and that may inadvertently factor in characteristics that it shouldn't, such as race. This is due to the fact that characteristics of the consumer, such as their use of technology, shopping habits, social-media practices, etc. likely vary by race. For example, 30% of whites use their mobile phone as their only form of Internet connection, compared to around 47% of Latinos and 38% of blacks [8]. As a result, when combined with other infomation, the way people use their mobiles and the Internet could be used as a proxy for race.

Even when data miners are careful, they can still produce models that unintentionally pick out proxy variables for protected classes. 

A possible effect of this *social credit score* is social segregation. In order to boost their credit score, a user may try to 'clean' their social media pages by, for example, unfriending certain people who have lower credit scores or refraining from liking pages that may give a 'bad impression' about them. 

>*"Those from disadvantaged backgrounds would interact only with users who, likewise, have not been able to break free of the cycle of poverty; Ivy League alumni would only allow themselves to be associated with similarly elite peers; an executive wishing to virtually follow an organization committed to helping poor families is likely to avoid creating a traceable connection between herself and the unfortunate, and for similar reasons may be reluctant to "like” the business page for her best friend’s debt refinancing company."* [7]

Studies highlight that online social networks allow new social ties to form, even with complete strangers [4]. As a result, the consequences of people perfecting their social media profile will most likely extend beyond "virtual realms" [7]. 

>*"Widespread online segregation caused by social financial ranking could also legitimize the idea that people should be valued by their economic standing, and that friendships should accordingly occur only among homogenous groups."* [7] 

##Partnerships
###JD.com

In 2015, ZestFinance announced that they were partnering with JD.com, the second biggest online retailer in China, in a joint venture, called JD-ZestFinance Gaia, to evaluate the risks of lending to consumers and small businesses across the country. 

This joint venture hopes to use "ZestFinance's experience of using thousands of non-traditional data points to assess a borrower's ability to repay, with a vast trove of information on online shopping habits gleaned from JD.com’s 105 million active users" [1].

###Baidu

In 2016, Baidu, which is a Chinese search-engine that has around 80% marketshare, invested in ZestFinance. This deal is part of an agreement that will allow Baidu to use ZestFinance's technology to develop a credit scoring platoform based on their search data [3]. Search data is equivalent to someone's thoughts, meaning that our *thoughts* are now being used as data to calculate credit scores. 

Merrill says that, although a number of fintech startups are trying to offer credit scoring using the internet and social media in Asia, this is the first time that search data has been used to "power" credit scoring [3].

##References

[1] Ben McLannahan. ZestFinance joins JD.com in China venture. *Financial Times,* June 2015. 

[2] Douglas C. Merrill, Shawn M. Budde, John W.L. Merrill, Lingyun Gu, and James P. McGuire. System and method for building and validating a credit scoring function, January 2015. 

[3] Jon Russell. Baidu invests in ZestFinance to develop search-powered credit scoring for China. *TechCrunch*, July 2016.

[4] Daria Kuss and Mark Griffiths. *Online Social Networking and Addiction - A Review of the Psychological Literature,* volume 8. September 2011. 

[5] Mikella Hurley and Julius Adebayo. Credit Socring in the Era of Big Data. *Yale Journal of Law and Technology.* 18(1):148-216, 2017. 

[6] Nassim N. Taleb. Beware the Big Errors of 'Big Data'. *Wired,* August 2013. 

[7] Nizan Geslevich Packin and Yafit Lev-Aretz. On Social Credit and the Right to be Unnetworked. *Columbia Business Law Review,* 339, February 2016. 

[8] Persis Yu, Jillian McLaughlin, and Marina Levy. Big Data, a Big Disappointment for Socring Consumer Creditworthiness. Technical report, National Consumer Law Center, March 2014. 

[9] Quentin Hardy. Big Data for the Poor. *The New York Times,* July 2012. 

[10] Quentin Hardy. Just the Facts. Yes, All of Them. *The New York Times,* March 2012. 

[11] Upturn. Led Astray. Online Lead Generation and Payday Loans. Technical report, October 2015. 

