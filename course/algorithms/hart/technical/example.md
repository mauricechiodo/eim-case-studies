---
title: Example Page
template: LeafPage
---

# Example of branch creation

Consider a tree that tries to determine if a number is prime. The sample has been picked (with replacement) from a large database of integers and the attributes shown are those that have been picked (without replacement) from the set of attributes in the integer database.

TABLE OF INPUTS GOES HERE

## Formulae

$$\text{Entropy}(S)=-p\_\oplus\log\_2(p\_\oplus)-p\_\ominus\log\_2(p\_\ominus)$$

$$\text{Gain}(S,A)=\text{Entropy}(S)-\sum\_{v\in\text{values}(A)}\left(\frac{|S\_v|}{|S|}\centerdot\text{Entropy}(S\_v)\right)$$

## Creating the branch

$S=\\{1,2,2,4,7,9,9,9,13,16,17\\}$. The set of attributes $\mathbb{A}=\\{\text{Even?,}\leq8\text{?,}=k^2\\}$. The attributes $A\in\mathbb{A}$ are all booleans so $A=\\{0,1\\}$. Denote $\text{Even?}\equiv\mathbb{E}$, $\leq8?\equiv\mathbb{L}$ and $=k^2?\equiv\mathbb{S}$.

*These sets needn't all be booleans. An attribute could be, for example, "Is the number $0\leq n\leq6$ or $6<n\leq 10$  or not?"*

### Initial Entropy

$p\_\oplus=\frac{5}{11}$ (there are $5$ primes and $11$ total numbers) and $p\_\ominus=\frac{6}{11}$ so the initial entropy is

$$\text{Entropy}(S)=-\frac{5}{11}\log_2\left(\frac{5}{11}\right)-\frac{6}{11}\log_2\left(\frac{6}{11}\right)\approx0.994$$

This is almost as entropic as it can be. To calculate the gain, take all the atributes $A\in\mathbb{A}$ and calculate their individual gains. Using $\mathbb{E}=\\{0,1\\}$ as an example

$$\text{Gain}(S,\mathbb{E})=\text{Entropy}(S)-\underbrace{\frac{4}{11}\cdot\text{Entropy}(S\_1)}\_{\text{Relative entropy of the even numbers}}-\underbrace{\frac{7}{11}\cdot\text{Entropy}(S\_0)}\_{\text{Relative entropy of the odd numbers}}$$
