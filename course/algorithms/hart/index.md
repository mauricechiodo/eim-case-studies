---
Title: HART
Template: LeafPage
---

## HART

oauanthbutnoauntoemu

HART -- the Harm Assessment Risk Tool -- is an algorithm designed to acess how much of a risk an offender poses to their community. This will help determine if the offender should be released with bail and how much help they should recieve when re-intergrating into society. HART functions using the machine learning process of *random forests*, a method by which many algorithms are generated and there is a first past the post vote between all of them.

### Random Forests

*Random Forests* are a machine learning method that involves training many trees to each produce their own algorithm for categorising inputs. Let $\mathbb{T}$ be the set of trees, $\mathbb{I}$ be the space of all inputs and $\mathcal{O}$ be the outputs, then in \textsc{hart} $T_k\in\mathbb{T}$ is a function

$$T_k:\mathbb{I}\to\mathcal{O}$$

Each individual tree is developed over a subset of the total data, optimised over some conditions, to form a forest $\mathbb{T}=\{T_k:k\in[n]\}$ for some $n$.

The random forest \textsc{ai} computes designation $R$ of an input ${\bf I}\in\mathbb{I}$ with the technology

$$R=\max_{o\in\mathcal{O}}\left(\left|\{T\in\mathbb{T}:T({\bf I})=o\}\right|\right)$$

So, for example, \textsc{hart} has $\mathcal{O}=\{$'High-risk','Medium-risk','Low-risk'$\}$
