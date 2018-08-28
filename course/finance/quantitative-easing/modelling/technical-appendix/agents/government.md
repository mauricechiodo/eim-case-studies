---
Title: Government Policy
Template: LeafPage
---

# Government policies
$\newcommand{\F}[1]{^{[\text{F}#1]}}$$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$$\newcommand{\c}[1]{^{[#1]}}$$\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$
-   $\Pi\_t\equiv\frac{P\_t}{P\_{t-1}}$ is the **inflation rate**.

-   $\epsilon\_{m,t}$ is an **iid innovation**, where $m\in\{B,T\}$.
    This dictates a shock increase in some of the following equations.

-   $G\_t$ is **taxes of a perpetuity**, costs associated with
    perpetuities manifest by this variable.

The government has an interest rate that feeds back on itself$\F{1}$, the
returns $R\_t$ on bonds follows the equation

$$\frac{R\_t}{R}=\left(\frac{R\_{t-1}}{R}\right)^{\rho\_m}\left[\left(\frac{\Pi\_t}{\Pi}\right)^{\phi\_\pi}\left(\frac{Y\_t/Y\_{t-4}}{e^{4\gamma}}\right)^{\phi\_y}\right]^{1-\rho\_m}e^{\epsilon\_{m,t}}$$

Where $\rho\_m\in(0,1),\phi\_\pi>1$ and $\phi\_y\geq0$. This is the last
step’s return $\frac{R\_t}{R}$ decayed by some power $\rho\_m$ times an
expression that relates the change to how much products are growing and
inflation, all times some shock $\epsilon\_{m,t}$. The government’s
budget constraint is naturally

$$B\_t+P\_{L,t}B\_t^L=R\_{t-1,t}B\_{t-1}+(1+\kappa P\_{L,t})B\_{t-1}^L+P\_tG\_t-T\_t$$

Thus the left hand side is money given to the government from bonds
sold, short and long-term. The right hand side is money paid back from
bonds maturing, or upkeep on perpetuities, plus tax.\
It is assumed that long-term bonds are controlled by the government
following an auto-regressive model with a shock factor

$$\frac{P\_{L,t}B\_t^L}{P\_tZ\_t}=\left(\frac{P\_{L,t-1}B\_{t-1}^L}{P\_{t-1}Z\_{t-1}}\right)^{\rho\_B}e^{\epsilon\_{B,t}}$$

Where $\rho\_B\in(0,1)$ so as $t\mapsto\infty$ the proportion of
perpetuity to productivity will converge to $1$, assuming
$\epsilon\_{B,t}$ remains at $0$ the whole time.\
The government adjusts the **real primary fiscal surplus**, a
measure of how much real wealth the government has spare, by considering
that there is lagged real-value long-term debt from perpetuities.

$$\frac{T\_t}{P\_tZ\_t}-\frac{G\_t}{Z\_t}=\Phi\left(\frac{P\_{L,t-1}B\_{t-1}^L}{P\_{t-1}Z\_{t-1}}\right)^{\phi\_T}e^{\epsilon\_{T,t}}$$

The constant $\Phi$ is chosen such that this is identically true in
steady state. $\phi\_T>0$

---

# Footnotes

$\F{1}$ That is to say the interest rate today influences the interest rate tomorrow.
