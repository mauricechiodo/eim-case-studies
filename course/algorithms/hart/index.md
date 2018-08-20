---
title: HART
template: LeafPage
---

# HART
$\newcommand{\F}[1]{^{[\text{F}#1]}}$
$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$
$\newcommand{\c}[1]{^{[#1]}}$

HART - the Harm Assessment Risk Tool - is an algorithm designed to acess how much of a risk an offender poses to their community. HART functions using the machine learning process of *random forests*, a method by which many algorithms are generated and there is a first past the post vote between all of them.

## Background - Checkpoint

Checkpoint is an initiative within the Durham constabulary that seeks to tackle the root causes of crime and the effect that has on the community.$\C{3}{227}$ The program allows offenders, as an alternative to going to prosecution, to enter a contract.$\F{1}$ A specialist 'navigator' assesses the offender and draws up a contract that may include these conditions

* Offending condition – not to reoffend over the period of the contract. (mandatory condition)
* Victims condition – to take part in a Restorative Approach if asked, to put right the harm caused.
* Pathway Condition – Interventions around issues that contributed to the subject committing the offence.
* Pathway Condition – Interventions around issues that contributed to the subject committing the offence.
* Complete 18-36 hours voluntary work in the community or wear a GPS tag.

*List from Durham Police website*$\c{2}$

Should the offender fail to complete their contract, they are taken to court. Only offenders which are categorised by HART as being medium-risk are eligible to enter the Checkpoint program, that is to say, only those predicted to commit a non-serious offence in the next 24 months.

## Random Forests

*Random Forests* are a machine learning method that involves training many trees to each produce their own algorithm for categorising inputs. Let $\mathbb{T}$ be the set of trees, $\mathbb{I}$ be the space of all inputs and $\mathcal{O}$ be the outputs, then in HART $T_k\in\mathbb{T}$ is a function

$$ T_k:\mathbb{I}\to\mathcal{O} $$

Each individual tree is developed over a subset of the total data, optimised over some conditions, to form a forest $\mathbb{T}=\\{T_k:k\in[n]\\}$ for some $n$.

The random forest AI computes designation $R$ of an input ${\bf I}\in\mathbb{I}$ with the technology
$$ R=\max_{o\in\mathcal{O}}\left(\left|\{T\in\mathbb{T}:T({\bf I})=o\}\right|\right) $$

So, for example, HART has $\mathcal{O}=${'High-risk','Medium-risk','Low-risk'}$\C{3}{228}$

---
# Footnotes

$\F{1}$ This does not apply to serious offences, such as rape, robbery or murder. Hate crime, domestic abuse and driving offences also disqualify an offender from Checkpoint.

---
# Bibliography

$\c{1}$ Sheena Urwin. “Algorithm Forecasting of Offender Dangerousness for Police Custody Officers: An Assessment of Accuracy for the Durham Constabulary Model”. In: (2016-12), p. 136. url: http://www.crim.cam.ac.uk/alumni/theses/Sheena%20Urwin%20Thesis%2012-12-2016.pdf (visited on 2018-08-07).

$\c{2}$ *Checkpoint*. url: https://www.durham.police.uk/Information-and-advice/Pages/Checkpoint.aspx (visited on 2018-08-20).

$\c{3}$ Marion Oswald et al. “Algorithmic risk assessment policing models: lessons from the Durham HART model and ‘Experimental’ proportionality”. In: *Information & Communications Technology Law* 27.2 (2018-05-04), pp. 223–250. issn: 1360-0834, 1469-8404. doi: 10.1080/13600834.2018.1458455. url: https://www.tandfonline.com/doi/full/10.1080/13600834.2018.1458455 (visited on 2018-08-07).
