---
Title: CDOs and the Financial Crisis
Template: LeafPage
---

#CDOs and the Financial Crisis

>*"In the world of finance, too many quants see only the numbers before them and forget about the concrete reality the figures are supposed to represent."* - Salmon in 'Recipe for Disaster: The Formula that Killed Wall Street'

Li made one big simplification in his model. He didn't just drastically decrease the difficulty of calculating correlations; furthermore, he decided not to calculate all the relationships between the various loans that made up the underlying pool. In Li's model, the only thing that mattered was the final correlation number.
 
>*"The effect on the securization market was electric."* - Salmon in 'Recipe for Disaster: The Formula that Killed Wall Street'

Now, investment bankers could package anything up into a CDO - corporate bonds, bank loans, mortgage-backed securities, etc. - and turn it into a triple-A rated security, although none of the individual components were triple-A rated. 

Furthermore, they could even take lower rated tranches of CDOs to create a CDO. This become known as a CDO-squared. These were so far removed from the original underlying bonds, loans or mortgages that no one really knew exactly what they were made up of. But, this didn't matter to investment bankers because they had Li's copula function. 

Although CDOs were first presented in the 1980s, there was a massive growth in their issuance from 2001. This was when rating agencies became more familiar with CDOs, and so they started to receive ratings. In 2004 the worldwide CDO issuance was \$97 billion, peaking in 2006 when it totaled to \$445 billion. And, at the heart of it all was Li's formula. Below is a graph depicting CDO issuance according to primary collateral type (USD millions).

![CDO issuance according to primary collateral type (USD millions)](/course/media/Figure5.png "CDO issuance according to primary collateral type (USD millions)")

Li's model could be applied anywhere, for anything and so was quickly adopted by, not only banks who wanted to package new bonds, but also hedge funds who wanted to make complex trades between those bonds. 

As the copula function used credit default swap prices to calculate correlation, it could only get data from the period of time when credit default swaps existed, which was less than a decade. During this period, the default correlations were very low. Bilginsoy (2014) highlights how when *The Economist* in 2003, and other print media, questioned whether the US housing market was experiencing a bubble and whether higher prices were sustainable, experts assured that a "generalized price bubble and implosion were unlikely".

However, the bubble eventually burst. The supply of houses caught up with speculative demand causing a decline in the value of homes. Futher, the honeymoon period of adjustable-rate mortgages (see [glossary](/course/course/finance/cdos/glossary) had passed, which resulted in many borrowers facing large increases in their mortgage payments as the interest rates were reset [4]. This caused many homeowners to have a mortgage debt that was greater than the value of their home. As a result, correlations skyrocketed. 

>*"Everyone was pinning their hopes on house prices continuing to rise"* - Kai Gilkes of CreditSights, a credit research firm. 

But, no one wanted to stop creating CDOs. So they kept building more and more using the data from credit default swaps that came from a period when the real estate prices had only gone up in order to calculate the default correlation.

When the US mortgage crisis happened in 2007, the issuance of CDOs fell dramatically and the premiums' issuers were willing to pay for credit protection increased dramatically. As of October 2008 the CDO market was frozen and 67% of the CDOs issued since late 2005 to middle 2007 were in formal state of default.

Problems with the CDO market started when mortgage backed securities investors suffered losses. As many CDOs were linked to these investors, their tranches were downgraded creating a spiral of losses. The downgrades of CDO tranches triggered losses of CDO investors, and further CDO tranches had to be downgraded causing further losses and write-downs. In total, writedowns by banks and other financial institutions between mid-2007 and May 2009 are estimated at $625 billion. To put this figure into perspective, it is **more** than the US Department of Defense base budget in 2007, which was $439.3 billion, as stated in the Budget of the U.S. Government in 2007.

The figure below shows the writedowns of top CDO issuers since mid 2007 until Februray 2009, taken from 'Crashes and collateralized lending' by Jurek and Stafford. 

![Top CDO issuers and their writedowns as of February 2009](/course/media/Figure3.png "Top CDO issuers and their writedowns as of February 2009")

These write-downs happened as a result of the high volume of subprime mortgages issued recklessly to households with a low credit scores in the US. The mortgages were securitised into mortgage back securities (MBS) and then sold to institutional investors. As a result, the credit risk of the mortgages was spread to the whole financial sector. Then, after some mortgage defaults the institutions involved were extremely affected, some of them even defaulting, such as Lehman Brothers or US mortgage agencies Fannie Mae and Freddie Mac. As stated by Calabria in 'Fannie, Freddie, and the Subprime Mortgage Market', these two mortgage agencies were so heavily affected because during the housing bubble in 2003-2004, when the level of private-label securitisations increased by over 50%, they owned almost 40% of newly issued private-label subprime securities, making them the largest single source of liquidity for this market .

>*"Because of high interdependence within a financial sector and its strong link to all business sectors, a series of problems of underlying companies led to a serious financial crisis the world is now experiencing."* -Teplý and Benesova in 'The Dark Side of Collateralized Debt Obligation's Valuation during the 2008/2009 Financial Crisis'.

Click [here] to see a video on the main flaws in the CDO Market.

----

*Include the information below in video:*

In 'The Dark Side of Collateralized Debt Obligation's Valuation during the 2008/2009 Financial Crisis', Teplý discusses the main flaws in the CDO market. 
	-**The Mark-to-Market Valuation Principle should be reconsidered.** Mark-to-Market is a measure of the fair value of accounts that can change over time, such as assets. It aims to give a realistic appraisal of an institution's or company's current financial situation. The Mark-to-Market valuation principle causes a problem as it creates the obligation to mark assets to market quotes, even if the they intend on holding the CDO to maturity.
	- **CDO investors did not undertake a deeper analysis of CDO underlying assets.** There was low diversification of underlying assets, which should have been reflected by rating agencies. Furthermore, the volume of CDOs issued on one bond exceeded the issued volume of the bond. The effects of this were that there was a massive chain reaction of downgrades and losses after just one default. 
	- **There was a misunderstanding of the valuation model.** The valuation models are based on fixed expected cashflows, and show the value for investors who hold a CDO to "maturity", and so should not be valued on the mark-to-market principle. *"If an investor bought a senior tranche, even after three defaults the chance of being hit was still very low and his cashflow would remain unchanged and therefore the basic idea of the model was correct."* [11] 
	However, the model didn't take into account mark-to-market losses. This should have been understood by investors, who have to disclose the mark-to-market value of their assets. Therefore, when there were huge mark-to-market losses triggered by the downgrades during the financial crisis, there was huge mispricing. 
	- **Correlation was mispriced in the model.** The implied and base correlations are derived from the CDO market quotes. Above we argued that there was mispricing, and so neither correlation value was correct. Only after there is a correct valuation of a CDO can the actual value of the correlation be derived. Hence, the market underestimated the high level of correlation among global markets and the speed of "contagion" to unaffected markets, causing a "whiplash" effect [11].

Despite clear flaws, the number papers that really address the issue of the CDO market incompleteness are very few [2] and are based on two different kinds of approaches: 
	- no-arbitrage pricing (e.g. [8] and [9]);
	- utility indifference pricing (e.g. [3], [7], [10])
 
Additionally, the paper 'From insurance risk to credit portfolio management: a new approach to pricing CDOs' [2] discusses a new approach for pricing collateralized debt obligations (CDOs) which takes into account the issue of the market incompleteness.

##References

[1] Mark A. Calabria. Fannie, Freddie, and the Subprime Mortgage Market. Technical Report 120, Cato Institute Briefing Paper, March 2011. 

[2] Alessandro Andreoli, Luca Vincenzo Ballestra, and Graziella Pacelli. From insurance risk to credit portfolio management: A new approach to pricing CDOs. *Quantitative Finance,* 16(10):1495-1510, April 2016.

[3] Guillaume Bernis. Mark-to-model for cash CDOs through indifference pricing. *Quantitative Finance*, 12(1):39-48, January 2012.

[4] C. Bilginsoy. *A History of Financial Crisis: Dreams and Follies of Expectations.* Economics as Social Theory. Taylor & Francis, 2014. 

[5] Bureau of the Budget and United States. Fiscal Year 2007. *Budget of the United States Government*, February 2006. 

[6] Felix Salmon. Recipe for Disaster: The Formula that Killed Wall Street. *Wired*, February 2009.

[7] Jakub W. Jurek and Erik Stafford. Crashes and collateralized lending. *National Bureau of Economic Research Working Paper Series,* 17422, September 2011. 

[8] Michael B Walker. An Incomplete-Market Model for Collateralized Debt Obligations. Department of Physics, University of Toronto, 2005. 

[9] Michael B Walker. CDO valuation: term structure, tranche structure, and loss distributions. Department of Physics, University of Toronto, January 2007. 

[10] Ronnie Sircar and Thaleia Zariphopoulou. Utility valuation of multi-name credit derivatives and application to CDOs. *Quantitative Finance,* 10(2):195-208, February 2010. 

[11] Petr Teplý and Petra Benesova. The Dark Side of Collateralized Debt Obligation's Valuation during the 2008/2009 Financial Crisis. Czech Republic, October 2009. 

