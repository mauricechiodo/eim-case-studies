---
Title: Obtaining the Marginal Distributions
Template: LeafPage
---

#Obtaining the Marginal Distributions

The following section is taken from ideas presented by Li (2000) 10.

##Characterisation of Default by Time-Until-Default

First we introduce a random variable called the \textbf{time-until-default} (or \textbf{survival time}) for a security to denote the length of time until default. 
To precisely determine this we need:
	- a time origin: current time;
	- a time scale for measuring the passage of time: in terms of years for continuous models, or numbers of period for discrete models;
	- a clear definition of default: defined by some rating agencies, such as Moody's.

##Survival Function

Consider an existing security A. This security's time-until-default $T$ is a continuous random variable, measuring the length of time from today to the time when default occurs. Let

	$F(t) = Pr(T \leq t)$, $t \geq 0$ and $S(t) = 1 - F(t)$
	
	$F(0) = 0$

$S(t)$ is called the **survival function** and gives the probability that a security will attain age $t$. 

For a security which has survived $x$ years, we want to discuss the future lifetime for this security. Hence, we define the following:

	$_tq_x = Pr(T - x|T > x), t \geq 0$ 
	
	$_tp_x = 1 -$$_tq_x$ 

	We interpret $_t q_x$ as the conditional probability that a security A will default within the next $t$ years, given that it survives $x$ years. 

	We note that $_tp_0 = S(t)$.

##Hazard Rate Function

The hazard rate function gives the instantaneous default probability for a security that has attained age $x$. It is an equivalent to $F(t)$ and $S(t)$ as a way to specify the distribution of time-until-default and is the one used most by statisticians. 

	$Pr(x < T \leq x + \Delta x) = \frac{F(x + \Delta x) - F(x)}{1 - F(x)}$
	
	$\approx \frac{f(x)\Delta x}{1 - F(x)}$
	
	where $f(x) = F'(x)$

We call the function 

	$h(x) = \frac{f(x)}{1 - F(x)}$

the **hazard rate function** and gives the value of the conditional probability density function of $T$ at exact age $x$, given it survives up until that time. 

By noting that $h(x) = -\frac{S'(x)}{S(x)}$ we see that

	$S(t) = \exp^{-\int_{0}^{t}h(s)ds}$


Using this:

	$_tp_x = \exp^{-\int_{0}^{t}h(s+x)ds} \Rightarrow$ $_tq_x = 1 - \exp^{-\int_{0}^{t}h(s+x)ds}$ (+)


Furthermore, the probabiltiy distribution function for $T$ is $f(t) = S(t)$x$h(t)$. 

**Typical Assumption:** hazard rate is a constant, $h$, over certain period such as [$x, x+1$]. 

Under this assumption, the density function is

	$f(t) = he^{-ht}$

Hence, time-until-default follows an exponential distribution with parameter $h$.

##Construction of the Credit Curve

In the context of characterising the distribution of time-until-default, the hazard rate function is called a credit curve. 

There exist 3 methods to obtain the credit curve for a given credit:
	- Obtaining historical default information from rating agencies;
	- Taking the Merton option theoretical approach;
	- Taking the implied approach using market prices of defaultable bonds or asset swap spreads.

**Obtaining Historical Default Information:**

Rating agencies like Moody's publish historical default rate studies regularly. As well as one-year default rates, they also present multi-year default rates. From these we can get the hazard rate function. 

The first marginal conditional default conditional probablity in year 1 is simply the one-year default probability. The other marginal conditional default probabilities can be obtained using the following recursion formula:

	$_{n+1}q_x -$$_nq_x +$$_np_x*q_{x+n}$
	
	$\Rightarrow q_{x+n} = \frac{_{n+1}q_x - _nq_x}{1 - _nq_x}$ 

If we assume a piecewise constant hazard rate function over each year, then we can obtain the hazard rate function using ($+$).  

\begin{figure}[H]
	\caption{ \cite{david_x._li_default_2000}}
	\includegraphics[width=10cm]{Figure11}
	\centering
\end{figure}

<p>
    <img src="http://db716.user.srcf.net/eim-case-studies/media/Figure11.png" alt>
    <em>Hazard Rate Function of B Grade Based on Moody’s Study (1997) 10</em>
</p>

\textbf{Using the Merton Model}

In 1974, Merton \cite{merton_pricing_1974} used diffusion processes to describe the value of the firm and showed that a firm's default could be modeled with the Black and Scholes methodology. He showed that stock could be considered to be a call option on the firm with strike price equal to the face value of a single payment debt.

Using this framework, we can obtain the default probability for the firm over one period. We can translate this default probability into a hazard rate function. 

Geske (1977) \cite{geske_valuation_1977} and Geske and Deliaedis (1998) \cite{robert_geske_credit_1998} extended Merton's analysis to produce a term structure of default probabilities. As a result, we can use the relationship between the hazard rate and the default probabilities to obtain a credit curve.

\textbf{Using Market Observable Information}

This is the approach taken by most credit derivative trading tasks because the extracted default probabilities reflect the current market-agreed perception about the future default tendency of the underlying credit. 

In 1998, Li presented one approach to building the credit curve from market information.  \cite{david_x._li_constructing_1998} 

In summary, Li first assumes that there exist a series of bonds with maturity $1, 2, ..., n$ years, which are issued by the same company and have the same seniority. All of those bonds have observable market prices from which we can calculate their yields to maturity in order to obtain a yield spread curve over treasury (or asset swap spreads for a yield spread curve over LIBOR). 

The credit curve construction is then based on this yield spread curve and an assumption about the recovery rate based on the seniority and rating of the bonds, and the industry/corporation. 

In the paper by Li (2000) \cite{david_x._li_default_2000}, market information is used rather than historical information due to the following reasons:
\begin{itemize}
	\item The calculation of profit and loss for a trading desk can only be based on current market information as it reflects the market agreed perception about the evolution of the market in the future, which is what the actual profit and loss depends on;
	\item Rating agencies use classification variables that often omit some firm specific information. Constructing a credit curve for each credit allows us to use more firm specific information;
	\item Rating agencies react much slower than the market in anticipation of future credit quality;
	\item Ratings are primarily used to calculate default frequency rather than default severity. However, a lot of the value of a credit derivative depends on both;
	\item Information available from a rating agency is usually the one year default probability for each rating group and the rating migration matrix, but neither are necessarily stable over long periods of time. 
\end{itemize} 
