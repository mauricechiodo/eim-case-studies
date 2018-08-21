---
Title: Copula Models
Template: LeafPage
---

#Copula Models

Using Sklar's theorem we see that to construct a distributional model for a random vector X, it is sufficient to specify a copula model fitting to the data. 

A large variety of models have been developed and some of their properties have been investigated. The following questions are important to consider when deciding the how appropriate the Copula model is to the situation being modelled 17:
	- Is the range of dependence of these models wide and flexible enough?
	- Which of these models have tail dependence and are therefore able to model situations where there is strong positive dependence in tails?
	**Tail Dependence:** Suppose we have two random variables X and Y. Tail dependence is the probability that Y reaches extremely large values, given that random variable X attains extremely large values.
	Say we have two mortgages A and B for houses on the same road and A defaults - a very unlikely event. Then, given this, the probability that B will default is greater than 0. Hence, to model mortgages, we need a copula model with tail dependence. But, the Gaussian Copula does not, which was one of the major limitations for applying it to this context [click here for more information](http://db716.user.srcf.net/eim/course/finance/cdos/cdoeffectsdylan).

	
	
	\item Is there some parameter that can describe the degree of dependence?
	\item Is there some natural probabilistic interpretation of the model describing certain situations?
	\item Is there a closed form of the copula or a simple simulation algorithm that can be applied? 
\end{itemize}	

\subsection{Some Classes of Copulas}
In this section we present some classes of copulas, some of which are taken from chapter 1 of `Mathematical Risk Analysis' (2013) \cite{ludger_ruschendorf_copulas_2013} and others were discussed by Li (2000) \cite{david_x._li_default_2000} before ultimately choosing the Gaussian copula.

\subsubsection{Farlie--Gumbel--Morfenstern (FGM) Copula}

The Farlie--Gumbel--Morfenstern (FGM) Copula is:

\hspace{12ex}$C_\alpha(u,v) = uv(1 + \alpha(1-u)(1-v)), |\alpha| \leq 1$

There are also its generalised versions - EFGM copulas, which are extensions of FGM to the $n$-dimensional case. They're given by:

\hspace{12ex}$C(u) = \prod_{i=1}^nu_i(1 + \sum_{T \subset \{1,..., n\}}\alpha_T\prod_{j \in T}(1-u_j))$ 

for suitable $\alpha_T \in \mathbb{R}^1.$

Some examples of applications of this family of copulas is  \cite{chin_diew_lai_distributions_2009}.: 
\begin{itemize}
	\item fitting data on the joint occurrence of certain trace elements in water;
	\item a starting point when considering how a population probability distribution function is altered in the surviving and nonsurviving groups by a risk function;
	\item reanalysing
	datasets on the effects of mixtures of
	poisons.
\end{itemize}

\subsubsection{Archimedean Copulas}
Archimedean Copulas are of the following form:

\hspace{12ex}$C_{\Phi}(u_1,...,u_n) = \Phi^{-1}(\Phi(u_1) + ... + \Phi(u_n))$

for some generator $\Phi: (0,1] \rightarrow \mathbb{R}_+)$ with $\Phi(1) = 0$ such that $\Phi$ is completely monotone. 

When $\Phi(t) = \frac{1}{\alpha}(t^{-\alpha} - 1)$ we get the \textbf{Clayton copula}:

\hspace{12ex}$C_\alpha(u) = (\sum u_i^{-\alpha}-n+1)^{-\frac{1}{\alpha}}, \alpha > 0$

When $\Phi_\delta(t) = -\frac{1}{\delta}\log(1 - (1-e^{-\delta})e^{-t})$ we get the \textbf{Frank copula}:

\hspace{12ex}$C_\delta(u) = -\frac{1}{\delta}\log(1 + \frac{\prod_{i = 1}^n(e^{-\delta u_i}-1)}{(e^{-\delta}-1)^{n-1}})$

Archimedean copulas are popular in practivce as they allow modeling dependence in arbitrarily high dimensions with only one parameter that determines the strength of dependence.

\subsubsection{Bivariate Normal}
The formula for the Bivariate Normal Copula is 

\hspace{12ex}$C(u,v) = \Phi_2(\Phi^{-1}(u), \Phi^{-1}(v), \rho), -1 \leq \rho \leq 1$

where $\Phi_2$ is the bivariate normal distribution function with correlation coefficient $\rho$, and $\Phi^{-1}$ is the inverse of a univariate normal distribution function. 

\subsubsection{Bivaraite Mixture Copula Function}
We can form a new copula function using existing copulas. 

If two uniform random vairable $u$ and $v$ are independent, we have a copula function $C(u,v) = uv$. If two random variables are perfectly correlated we have the copula function $C(u, v) = \min(u,v)$. 

Mixing the two copula functions above by a mixing coefficient ($\rho > 0$) we obtain a new copula function as follows:
\begin{itemize}
\item$C(u,v) = (1 - \rho)uv + \rho \min(u,v)$, if $\rho > 0$. 

\item$C(u,v) = (1+\rho)uv - \rho(u - 1 + v)\Theta(u - 1 +v)$, if $\rho \leq 0$

where 

\hspace{12ex} $\Theta(x) = 1$, if $x \geq 0$

\hspace{17.5ex} $= 0$, if $x < 0$
\end{itemize}

\subsection{Gaussian Copula Function}
Leading up to the financial crisis, the Gaussian copula function was the most widely used model in pricing multi-name credit structures, such as CDOs, due to Li's model approach presented in his 2000 paper `On Default Correlation: A copula function approach' \cite{david_x._li_default_2000}. This Gaussian Copula Model is a bottom-up model, discussed in section 1.  

The Gaussian Copula uses Gaussian random variables instead of uniform random variables.

As presented in Li's paper \cite{david_x._li_default_2000}, letting $\Phi$ be the distribution function of the one-dimensional standard normal distribution and $\Phi_\Sigma^n$ the distribution function of the $n$-dimensional standard normal distribution with positive definite correlation matrix $\Sigma$, the $n$-dimensional Gaussian copula $C_\Sigma^\Phi$ can be defined as:
\begin{center}
	$C_\Sigma^\Phi(u_1, ..., u_n) = \Phi_\Sigma^n(\Phi^{-1}(u_1), ..., \Phi^{-1}(u_n))$
\end{center}
for all $(u_1, ..., u_n) \in [0,1]^n$. 

Considering the simplest case where $n = 2$, we obtain:
\begin{center}
	$C_{p_{12}}^\Phi(u_1,u_2) = \int_{-\infty}^{\Phi^{-1}(u_1)} \int_{-\infty}^{\Phi^{-1}(u_2)}\frac{1}{2\pi(1-\rho^2_{12})^{\frac{1}{2}}}\exp[-\frac{s^2 - 2\rho_{12}*s*t + t^2}{2(1-\rho^2_{12})}]dsdt$
\end{center}
with $(u_1, u_2) \in [0,1]^2$ and $\rho_{12}$ being the correlation coefficient of the bivariate standard normal distribution.
