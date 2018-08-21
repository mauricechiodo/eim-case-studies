---
title: HART
template: LeafPage
---

# HART
$\newcommand{\F}[1]{^{[\text{F}#1]}}$$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$$\newcommand{\c}[1]{^{[#1]}}$$\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$

HART is an algorithm employed by the Durham constabulary as part of the *Checkpoint* program. It categorises, by the method of *random forests*, a suspect into three categories, which are *High-Risk*, *Medium-Risk* and *Low Risk*.$\Ci{1}{Section 6.1, p.15}$ These correspond to the severity of crime predicted to be committed over the next 24 months, respectively a serious offence, a non-serious offence and no offence. Only those categorised as medium-risk by HART may use the Checkpoint program.$\c{2}$

## The Model

HART is an machine-learning algorithm that was trained, as all are, to minimize its total cost of errors, where different errors produced have different costs associated with them. False-positives, in which a reoffender is erroneously identified as low-risk, are given a high cost since they are the most dangerous error the algorithm can make, whereas false-negatives are given a lower cost. In this way, HART seeks to minimize the danger to community while trying to still truly apply the data correctly.$\C{3}{228}$ The costs associated with each of these were set by the people who designed HART, thus having to make an arbitrary choice with ethical consequence.

Urwin used an independent dataset of 14822 past cases from Durham in 2013 to validate the algorithms effectiveness. The results from HART were then compared to the actual, known results of the suspect's behaviour over the next 24 months. The accuracy for this sample was 62.8%, less than the estimated 68.5%.$\C{3}{229}$

The model uses 34 predictors as inputs, including the suspect's truncated postcode and gender, to determine the output.$\Ci{1}{Appendix A, p.96-97}$ Most of these predictors (29) are directly related to the suspect's offending history.$\C{3}{228}$

One of the variables in the model is ```PriorSeriousOffenceLatestYears```, the 'number of years since the most recent custody instance in which a serious offence was committed'. If there is no prior offence, then a code of 100 years is used. It is unclear if the algorithm interprets this as having *never* committed a previous offence or if it interprets the input as it having been 100 years since last offence. The same code is used for many more specific types of offence, such as last sexual/drug/weapon offence.$\Ci{1}{Appendix A, p.99}$

## Background - Checkpoint

Checkpoint is an initiative within the Durham constabulary that seeks to tackle the root causes of crime and the effect that has on the community.$\C{3}{227}$ The program allows suspects, as an alternative to going to prosecution, to enter a contract.$\F{1}$ A specialist 'navigator' assesses the suspect and draws up a contract that may include these conditions

* Offending condition – not to reoffend over the period of the contract. (mandatory condition)
* Victims condition – to take part in a Restorative Approach if asked, to put right the harm caused.
* Pathway Condition – Interventions around issues that contributed to the subject committing the offence.
* Pathway Condition – Interventions around issues that contributed to the subject committing the offence.
* Complete 18-36 hours voluntary work in the community or wear a GPS tag.

*List from Durham Police website*$\c{2}$

Should the suspect fail to complete their contract, they are taken to court. Only suspects which are categorised by HART as being medium-risk are eligible to enter the Checkpoint program, that is to say, only those predicted to commit a non-serious offence in the next 24 months.

## Random Forests

*Random Forests* are a machine learning method that involves training many trees to each produce their own algorithm for categorising inputs. Let $\mathbb{T}$ be the set of trees, $\mathbb{I}$ be the space of all inputs and $\mathcal{O}$ be the outputs, then in HART $T_k\in\mathbb{T}$ is a function

$$ T_k:\mathbb{I}\to\mathcal{O} $$

Each individual tree is developed over a subset of the total data, optimised over some conditions, to form a forest $\mathbb{T}=\\{T_k:k\in[n]\\}$ for some $n$.

The random forest AI computes designation $R$ of an input ${\bf I}\in\mathbb{I}$ with the technology
$$ R=\max_{o\in\mathcal{O}}\left(\left|\{T\in\mathbb{T}:T({\bf I})=o\}\right|\right) $$

So, for example, HART has $\mathcal{O}=${'High-risk','Medium-risk','Low-risk'}$\C{3}{228}$

---
# Footnotes

$\F{1}$ This does not apply to serious offences, such as rape, robbery or murder. Hate crime, domestic abuse and driving offences also disqualify a suspect from Checkpoint.

---
# Bibliography

$\c{1}$ Sheena Urwin. “Algorithm Forecasting of Offender Dangerousness for Police Custody Officers: An Assessment of Accuracy for the Durham Constabulary Model”. In: (2016-12), p. 136. url: http://www.crim.cam.ac.uk/alumni/theses/Sheena%20Urwin%20Thesis%2012-12-2016.pdf (visited on 2018-08-07).

$\c{2}$ *Checkpoint*. url: https://www.durham.police.uk/Information-and-advice/Pages/Checkpoint.aspx (visited on 2018-08-20).

$\c{3}$ Marion Oswald et al. “Algorithmic risk assessment policing models: lessons from the Durham HART model and ‘Experimental’ proportionality”. In: *Information & Communications Technology Law* 27.2 (2018-05-04), pp. 223–250. issn: 1360-0834, 1469-8404. doi: 10.1080/13600834.2018.1458455. url: https://www.tandfonline.com/doi/full/10.1080/13600834.2018.1458455 (visited on2018-08-07).
