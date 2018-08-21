---
Title: Gaussian Copula Approach CDO tranche modelling
Template: ListSubPages
---

\section{Gaussian Copula Approach CDO tranche modelling}
In a typical CDO, if the correlation amongst the  bonds or loans in the pool was low, only the holders of the lowest tranche would be at a great risk of losing some or all of their investment. However, if the correlation was very high, many of the bonds or loans might default and so the losses could impact even the most senior tranche. As a result, modelling correlation was the most crucial problem in CDO evaluation, and Gaussian copulas became the most popular way to do this \cite{donald_mackenzie_formula_2014}. Below I will detail how to apply the Gaussian Copula to the problem of pricing CDO tranche as discussed by Li (2000) \cite{david_x._li_default_2000}.

Let $\tau_i$ be a random variable that describes the default time of the $i^{th}$ asset in the underlying pool and $F(t_1) = Pr(\tau_1 < t_1)$ the marginal default time distribution function for $i = 1, ..., M$, where $M$ is the number of assets in the pool. 

To model the joint default times of all the assets in the underlying pool $F(t_1, ..., t_M)$ for all $(t_1, ..., t_M) \in \mathbb{R}_+^M$, we make use of Sklar's theorem, which ensures the existence of a copula $C:[0,1]^M \rightarrow [0,1]$ such that 
\begin{center}
	$F(t_1, ..., t_M) = C(F_1(t_1), ..., F_M(t_M)).$ (**)
\end{center}
The most common used version of Li's model is the \textbf{One-factor Gaussian Copula Model} \cite{university_of_oxford_gaussian_2016}, as it offers ``high analytical tractability" (meaning it can be solved analytically in terms of a closed form expression) by assuming that the portfolio of the underlying assets is homogenous (see details of how this model was developed in the section `\textbf{Overview of what happened after Li's Paper, before the Financial Crisis}'). 

Each asset in the underlying portfolio belongs to a company $i$ with asset value $X_i$ for $i = 1, ..., M$. The one-factor framework means that the value of the company $i$ is modeled as 
\begin{center}
	$X_i = \sqrt{\rho}Y + \sqrt{1-\rho}Z_i$ for $i = 1, ..., M$
\end{center}
where $Y, Z_1, ..., Z_M$ are independent and identically distributed $N(0,1)$ random variables and $\rho \in (0,1)$. Here $Y$ describes a kind of market risk common to all companies, and $\{Z_i\}_{i = 1}^M$ present risks specific for each company $i$.

Now, $(X_1, ..., X_M)$ has a multivariate normal distribution with mean zero and a covariance matrix:

\begin{center}
$\begin{bmatrix}
	1 & \rho & \dots  & \rho \\
	\rho & 1 & \dots  & \rho \\
	\vdots & \vdots & \ddots & \vdots \\
	\rho & \rho & \dots  & 1
\end{bmatrix}$
\end{center}

One of the core assumptions of the model is that there is a flat correlation between each pair of companies due to the homogeneity of the asset pool. This leads to one value of $\rho$ for the correlation of every pair of assets. This is a very strong assumption and may not have been appropriate in the context of pricing CDOs. For example, suppose that in the underlying pool of assets of a CDO there exist the following:
\begin{itemize}
	\item Two mortgages A and B from the same street in the UK
	\item One mortgage C from a house in New York
\end{itemize}
Whilst the default correlation between A and C, and B and C may be very similar, it will not be similar to the default correlation between A and B; intuitively we can see that if A defaults, B is much more likely to default (and vice versa), whereas this event will likely have to consequence whether or not mortgage C defaults.

We say that a company $i$ defaults if their asset value $X_i$ is below a certain threshold. So we link the single default time $\tau_i$ to the one-factor model by the relation $X_i = \Phi^{-1}(F_i(\tau_i))$.

Then, after the marginal distribution functions $\{F_i\}_{i = 1}^M$ for the $\{\tau_i\}_{i = 1}^M$ are determined, we can use (**) and the Gaussian copula to estimate the joint default distribution of the asset pool. We have then fully specified the one-factor Li model.
