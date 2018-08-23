---
title: Example Page
template: LeafPage
---

# Example of branch creation
$\newcommand*{\defeq}{\mathrel{\vcenter{\baselineskip0.5ex \lineskiplimit0pt
                     \hbox{\scriptsize.}\hbox{\scriptsize.}}}%
                     =}$
Consider a tree that tries to determine if a number is prime. The sample has been picked (with replacement) from a large database of integers and the attributes shown are those that have been picked (without replacement) from the set of attributes in the integer database.

TABLE OF INPUTS GOES HERE

## Formulae

$$\text{Entropy}(S)=-p\_\oplus\log\_2(p\_\oplus)-p\_\ominus\log\_2(p\_\ominus)$$

$$\text{Gain}(S,A)=\text{Entropy}(S)-\sum\_{v\in\text{values}(A)}\left(\frac{|S\_v|}{|S|}\centerdot\text{Entropy}(S\_v)\right)$$

## Creating the branch

$S=\\{1,2,2,4,7,9,9,9,13,16,17\\}$. The set of attributes $\mathbb{A}=\\{\text{Even?,}\leq8\text{?,}=k^2\\}$. The attributes $A\in\mathbb{A}$ are all booleans so $A=\\{0,1\\}$. Denote $\text{Even?}\defeq\mathbb{E}$, $\leq8?\defeq\mathbb{L}$ and $=k^2?\defeq\mathbb{S}$.

*These sets needn't all be booleans. An attribute could be, for example, "Is the number $0\leq n\leq6$ or $6<n\leq 10$  or not?"*
