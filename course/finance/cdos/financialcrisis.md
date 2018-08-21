---
Title: CDOs and the Financial Crisis
Template: LeafPage
---

#CDOs and the Financial Crisis

\textit{``In the world of finance, too many quants see only the numbers before them and forget about the concrete reality the figures are supposed to represent."} \cite{felix_salmon_recipe_2009}
\end{center}

Li made one big simplification in his model. He didn't just drastically decrease the difficulty of calculating correlations, he decided not to calculate all the relationships between the various loans that made up the underlying pool. In Li's model, the only thing that mattered was the final correlation number.
 
\begin{center}
\textit{``The effect on the securization market was electric."} \cite{felix_salmon_recipe_2009}
\end{center}

Now, investment bankers could package anything up into a CDO - corporate bonds, bank loans, mortgage-backed securities, etc. - and turn it into a triple-A rated security, although none of the individual components were triple-A rated. 

Furthermore, they could even take lower rated tranches of CDOs to create a CDO. This become known as a CDO-squared. These were so far removed from the original underlying bonds, loans or mortgages that no one really knew exactly what they were made up of. But, this didn't matter to investment bankers because they had Li's copula function. 

Although CDOs were first presented in the 1980s, there was a massive growth in their issuance from 2001. This was when rating agencies became more familiar with CDOs, and so they started to receive ratings. In 2004 the worldwide CDO issuance was \$97 billion, peaking in 2006 when it totaled to \$445 billion. And, at the heart of it all was Li's formula.

\begin{figure}[H]
\includegraphics[width=10cm]{Figure5}
\centering
\caption{CDO issuance according to primary collateral type (USD millions) \cite{teply_dark_2009}}
\end{figure}

Li's model could be applied anywhere, for anything and so was quickly adopted by, not only banks who wanted to package new bonds, but also hedge funds who wanted to make complex trades between those bonds \cite{felix_salmon_recipe_2009}. 

As the copula function used credit default swap prices to calculate correlation, it could only get data from the period of time when credit default swaps existed, which was less than a decade. During this period, the default correlations were very low. When \textit{The Economist} in 2003, and other print media, questioned whether the US housing market was experiencing a bubble and whether higher prices were sustainable, experts assured that a ``generalized price bubble and implosion were unlikely" \cite{bilginsoy_history_2014}.

However, the bubble eventually burst. The supply of houses caught up with speculative demand causing a decline in the value of homes. Futher, the honeymoon period of ad
adjustable-rate mortgages (see glossary) had passed, which resulted in many borrwers facing large increases in their mortgage payments as the interest rates were reset \cite{bilginsoy_history_2014}. This caused many homeowners to have a mortgage debt that was greater than the value of their home. As a result, correlations sky-rocketed. 

\begin{center}
\textit{``Everyone was pinning their hopes on house prices continuing to rise''} 

- Kai Gilkes of CreditSights, a credit research firm. 
\end{center}

But, no one wanted to stop creating CDOs. So they kept building more and more using the data from credit default swaps that came from a period when the real estate prices had only gone up in order to calculate the default correlation \cite{felix_salmon_recipe_2009}.

When the US mortgage crisis happened in 2007, the issuance of CDOs fell dramatically and the premiums issuers were willing to pay for credit protection increased dramatically. As of October 2008 the CDO market was frozen and 67\% of the CDOs issued since late 2005 to middle 2007 were in formal state of default. \cite{teply_dark_2009} 

Problems with the CDO market started when mortgage backed securities investors suffered losses. As many CDOs were linked to these investors, their tranches were downgraded creating a spiral of losses. The downgrades of CDO tranches triggered losses of CDO investors, and further CDO tranches had to be downgraded causing further losses and write-downs. In total, writedowns by banks and other financial institutions between mid-2007 and May 2009 are estimated at \$625 billion \cite{teply_dark_2009}. To put this figure into perspective, it is \textbf{more} than the US Department of Defense base budget in 2007, which was \$439.3 billion \cite{bureau_of_the_budget_and_united_states_fiscal_2006}.

The figure below shows the writedowns since mid 2007 until Februray 2009. 

\begin{figure}[h]
	\centering
	\includegraphics[width=8cm]{Figure3}
	\caption{Top CDO issuers and their writedowns as of February 2009 \cite{teply_dark_2009}}
\end{figure}

These write-downs happened as a result of the high volume of subprime mortgages issued recklessly to households with a low credit scores in the US. The mortgages were securitised into mortgage back securities (MBS) and then sold to institutional investors. As a result, the credit risk of the mortgages was spread to the whole financial sector. Then, after some mortgage defaults the institutions involved were extremely affected, some of them even defaulting, such as Lehman Brothers or US mortgage agencies Fannie Mae and Freddie Mac. These two mortgage agencies were so heavily affected because during the housing bubble in 2003-2004, when the level of private-label securitizations increased by over 50\%, they owned almost 40\% of newly issued private-label subprime securities, making them the largest single source of liquidity for this market \cite{a._calabria_fannie_2011}.

\begin{center}
\textit{``Because of high interdependence within a financial sector and its strong link to all business sectors, a series of problems of underlying companies led to a serious financial crisis the world is now experiencing."} \cite{teply_dark_2009}
\end{center}

\subsection{Main Flaws in the CDO Market}
In `The Dark Side of Collateralized Debt Obligation's Valuation during the 2008/2009 Financial Crisis' \cite{teply_dark_2009}, Teplý discusses the main flaws in the CDO market. 
\begin{itemize}
	\item \textbf{The Mark-to-Market Valuation Principle should be reconsidered.} Mark-to-Market is a measure of the fair value of accounts that can change over time, such as assets. It aims to give a realistic appraisal of an institution's or company's current financial situation. The Mark-to-Market valuation principle causes a problem as it creates the obligation to mark assets to market quotes, even if the they intend on holding the CDO to maturity.
		
	\item \textbf{CDO investors did not undertake a deeper analysis of CDO underlying assets.} There was low diversification of underlying assets, which should have been reflected by rating agencies. Furthermore, the volume of CDOs issued on one bond exceeded the issued volume of the bond. The effects of this were that there was a massive chain reaction of downgrades and losses after just one default. 
	\item \textbf{There was a misunderstanding of the valuation model.} The valuation models are based on fixed expected cashflows, and show the value for investors who hold a CDO to ``maturity", and so should not be valued on the mark-to-market principle.
	
	``If an investor bought a senior tranche, even after three defaults the chance of being hit was still very low and his cashflow would remain unchanged and therefore the basic idea of the model was correct."\cite{teply_dark_2009}
	
	However, the model didn't take into account mark-to-market losses. This should have been understood by investors, who have to disclose the mark-to-market value of their assets. Therefore, when there were huge mark-to-market losses triggered by the downgrades during the financial crisis, there was huge mispricing. 
	\item \textbf{Correlation was mispriced in the model.} The implied and base correlations are derived from the CDO market quotes. Above we argued that there was mispricing, and so neither correlation value was correct. Only after there is a correct valuation of a CDO can the actual value of the correlation be derived. Hence, the market underestimated the high level of correlation among global markets and the speed of ``contagion" to unaffected markets, causing a ``whiplash" effect. \cite{teply_dark_2009}
\end{itemize}
Despite clear flaws, the number papers that really address the issue of the CDO market incompleteness are very few \cite{alessandro_andreoli_insurance_nodate} and are based on two different kinds of approaches: 
\begin{itemize}
	\item no-arbitrage pricing: \cite{michael_b_walker_incomplete-market_2005} and \cite{michael_b_walker_cdo_2007};
	\item utility indifference pricing: \cite{bernis_mark--model_2012}, \cite{jakub_w._jurek_crashes_2011} and \cite{sircar_utility_2010}.
\end{itemize}  
Additionally, the paper `From insurance risk to credit portfolio management: a new approach to pricing CDOs' \cite{alessandro_andreoli_insurance_nodate} discusses a new approach for pricing collateralized debt obligations (CDOs) which takes into account the issue of the market incompleteness.
