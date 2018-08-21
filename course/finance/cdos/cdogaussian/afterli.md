---
Title: Overview of what happened after Li's Paper, before the Financial Crisis
Template: LeafPage
---

#Overview of what happened after Li's Paper, before the Financial Crisis

MacKenzie (2014) \cite{donald_mackenzie_formula_2014} depicts the events that occured after the publication of `On Default Correlation: A copula function approach' (2000) \cite{david_x._li_default_2000}. 

There was one main limitation in Li's work: in practical applications, no analytical solution could be found, so computationally-intensive Monte Carlo simulation was needed. This had major consequences in investment banking.

In the early 2000s, new versions of CDOs became popular. These new versions of CDOs included `synthetic' single-tranch CDOs, which were simply bilateral contracts between an investment bank and a client that mimicked the returns and risks of a CDO tranche (rather than consisting of a special-purpose legal vehicle that bought a pool of debt instruments).
	
As the bank didn't own the pool of loans or bonds underpinning the contract, they had to find other ways of protecting against the losses throughout the contract's lifetime. This involved using credit default swaps (see glossary) on each of the corporations whose debts made up the pool. The hedge ratios that were needed in these credit default swaps were called `deltas'.

Investment bankers needed to recalculate these deltas daily, meaning that the computational demands of Monte Carlo simulation were a major problem. Hence, investment bankers became very interested in creating full-fledged copula formulations.
	
In an effort to develop `semi-analtical' versions of the Gaussian and other copulas, they made simplifications. A commonly used simplification, introduced by Gregory and Laurent (2001) of BNP, was to assume that the correlations among the asset values or default times of the corportations in a CDO pool all arose from their common dependence on one or more underlying factors. Most common of all was to assume a single underlying factor i.e. the One-Factor Gaussian Copula Model. 

\begin{center}
\textit{``The advantage of doing this was that given a particular value of the underlying factor,
defaults by different corporations could then be treated as statistically independent events, simplifying the mathematics, avoiding Monte Carlo simulation and greatly reducing computation times."} \cite{donald_mackenzie_formula_2014}
\end{center}

So, in order to be able to trade CDOs, they had to make lots of simplifications to Li's original model until computational times were low enough so that they could trade. Yes, this simplified model gave a mathematically true answer, but did it still have any meaning in the real world? Did the simplified model still price CDOs appropriately? A recent discussion with a trader revelead that, to do their job, traders ``choose the easiest model that works". However, as can be seen by the financial crisis of 2007/2008, this model clearly did not work.


Reducing the number of factors became a common technique used by quants. As a result single-factor, semi-analytical Gaussian copula models became very widely used in investment banking. 

In 2003-2004, investment banks collectively created tranched `index markets', which were effectively a set of standardised single-tranche synthetic CDOs with the same underlying pool of corporate debt issuers. As they were standardised they could be readily bought and sold, and therefore had credible market prices. 

These market prices gave a new way of determining the correlation $\rho$, turning it from a difficult task to an easy modelling job. This is because you could simply assume a common level of correlation between corporations in the pool underlying a standardised index and then run the Gaussian copula model backwards to get the level of correlation consistent with market prices. 

Running the Gaussian Copula model backwards to determine the ‘implied correlation’, i.e. the correlation level consistent with prices in the index market was done rather than trying to directly calculate correlation - a model full of difficulties. This was done just as, for example, an options model could be run backwards in order to estimate the implied volatility.

In fact, correlation was no longer just a parameter of a model but became something that could be traded in the new markets.

There was still one problem with this. Running the Gaussian copula model backwards sometimes gave two values, and in others cases no correlation value could be generated (see figure below).

\begin{figure}[H]
	\caption{Source: `Gaussian Copula Model, CDOs and the Crisis' \cite{university_of_oxford_gaussian_2016} ``DJ iTraxx Europe 5-year 3-6\% Tranche spread in bp (y axis), Input Correlation (x axis), as of 2004/02/16."}
	\includegraphics[width=10cm]{Figure12}
	\centering
\end{figure}

This could be avoided if the \textbf{base correlation method} was used. 

Before we discuss what the base correlation method was I will describe the basic structure of a CDO, as explained by Marcantoni in `Collateralized Debt Obligations' \cite{enrico_marcantoni_collateralized_2014}.
Each CDO is split into tranches. Each tranche is characterised by a lower limit called the \textit{attachment point} and an upper limit called the \textit{detachment point}. These express the percentage of
the total portfolio loss covered by the tranches. Usually the equity tranche is
characterized by an attachment point at zero. The detachment point for each tranche overlaps with the attachment point of the subsequent (in terms of degree of seniority) tranche. Consider a tranche with attachment and detachment point at $L$ and $U$ respectively. The holder of the tranche will responsible for the asset pool losses exceeding $L$ and then up to $U$. Due to this, they will not suffer any loss when the total portfolio losses are lower than $L$ and will not be liable for the part of losses greater than $U$. 

The main idea behind the base correlation method is to decompose all tranches into combinations of base trances. The word base comes from the fact that the attachement point of a base tranche is always zero. 

Consider the following example of a tranche with attachment and detachement points $K_1$ and $K_2$. This is equivalent to being short the equity tranche with upper attachment point $K_1$ and long the equity tranche with upper attachment point $K_2$.

\begin{figure}[H]
	\caption{Source: `Base Correlation Explained'\cite{dominic_okane_base_2004}}
	\includegraphics[width=12cm]{Figure13}
	\centering
\end{figure}
See `Base Correlation Explained' by O'Kane and Livesey (2004) \cite{dominic_okane_base_2004} for more detail on how the base correlation method works. 

Hence, by 2004-2005 investment bankers had managed to construct the canonical set of models: Gaussian copula base correlation models. 
