---
Title: Algorithmic Policing and Decision Making
Template: ListSubPages
GridImage: media/fairness-thumbnail.png
---

$\newcommand{\F}[1]{^{[\text{F}#1]}}$
Algorithms more and more are being used in policing situations, from the allocation of police resources to the sentencing of individuals for time in prison. Should they be effective, an algorithm would be a marvellous way to efficiently employ a just system of control over a population, able to churn through years of data to spot patterns that humans would never find. However, algorithms made with arbitrary humans are **not** impartial. Mathematicians producing algorithms that will have such a huge impact on people's lives as this need to be aware of and think about the decisions they are implicitly making by producing such algorithms.

[PredPol](/course/algorithms/predpol) is one such program that pre-emptively predicts where crime will occur and allows police forces to patrol those areas, rather than areas at random. The statistics show that using PredPol increases the amount of crime noticed and prevented than not using it - but at what cost? The data used in training PredPol will almost certainly be biased, since police forces around the world have repeatedly and astonishingly shown that their officers target people of colour more than anyone else. PredPol will pick up on high numbers of arrests in black neighbourhoods$\F{1}$, thus producing more arrests there due to increased traffic and more data to justify sending officers there. Mathematics has been mishandled to catch criminals at the cost of equality.

[HART](/course/algorithms/hart) is an algorithm currently employed by the Durham UK constabulary. It categorises a suspect into three categories based on how likely they are to commit (violent) crimes once released. There is machine learning used to generate *random forests*, a known contemporary method of constructing an AI. However, out of fear of releasing a violent criminal before their trial, the algorithm has been given heavy insentive to miscategorise people as being higher risk than they are. The justice system is designed to have people be assumed innocent until proven guilty, but at this level mathematics is being used to perverse that idea.

[COMPAS](/course/algorithms/compas) is an algorithm used widely to help determine the sentences that suspects should be given. The algorithm uses mathematically trivial methods to produce deciles for each of 3 categories.$\F{2}$ These have been used to justify longer sentences, and an attempt to scrutinize the algorithm was overruled in Loomis v Wisconsin. With this, mathematics is being used to sentence people.

---

# Footnotes

$\F{1}$ Especially in countries such as the United States, in which racial segregation in housing is huge.

$\F{2}$ Non-recidivism, recidivism and violent recidivism.
