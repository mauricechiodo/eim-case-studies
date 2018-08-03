---
Title: COMPAS
---

**COMPAS**

Algorithms have been used for determining prison sentences in several US states, beginning in the present decade. Among the most notorious algorithms is COMPAS, produced by the firm Northpointe; initially intended for determining probation periods (Brennan et al., 2009), it soon went into use for determining sentence lengths for convicted criminals, most notably in Wisconsin. Concerns, as in the Loomis case (State of Wisconsin v. Loomis, 2016) have been raised over the fact that the software is closed-source.

However, the greatest controversy arose when a ProPublica investigation suggested that the software was biased against black people (Angwin et al., 2016), primarily drawing on inconsistencies across the races in the flagging of false positives and false negatives in a dataset based on a single Florida county. There have, however, been numerous ripostes to their investigation (for instance Flores et al., 2016) accusing it of misrepresenting statistics; indeed, criticisms which I shall later describe have been levelled at it which suggest that their argument is mathematically incoherent.  


*Mathematics*

The mathematical basis behind COMPAS is not, it seems, especially profound. The primary risk assessment score, the ‘Violent Recidivism Risk Scale’, is calculated merely as a weighted average of five collated characteristics (Pr. Gd. COMPAS Core, 2015). (Even on this level, it is not particularly good – Dressel and Farid (2018) found that using just two variables rather than COMPAS’s 137 can given the same level of prediction accuracy.)  At the end of that section of the guide, there is a cursory note that “we would expect staff to disagree with an actuarial risk assessment (e.g. COMPAS) in about 10% of the cases”, but in perhaps the most infamous use of the software, the Loomis case, COMPAS was treated as though it were objective; the judge claimed that “the risk assessment tools that have been utilized, suggest that you're extremely high risk to re-offend” (State of Wisconsin v. Loomis, 2016). 

From a mathematical standpoint, there are two especially interesting papers that have arisen in the wake of this controversy. The first, by Lum and Johndrow, gives a technical definition of ‘fair’ and goes on to provide a prediction method, analogous in purpose to COMPAS, which is guaranteed to be ‘fair’ (in their specific sense) to both races. Indeed, their proposed method on unadjusted data had an AUC accuracy of 0.71, compared to 0.70 for COMPAS itself on the same dataset (Johndrow, 2016). (On adjusting the initial data using a ‘random forest’ machine learning method, this figure improved slightly to 0.72.) Although this was published on arXiv and has not appeared in a peer-reviewed journal, the mathematics appears sound. 

However, this focuses only on one potential definition of fairness. Another paper from the same year by Kleinberg, Mullainathan and Raghavan gives three definitions for fairness: the first is essentially similar to the one used by Johndrow, while the other two arise from similarly reasonable comparison of the data for white and black people. Notably, their paper shows that except for two very specific (and, indeed, unrealistic) cases, these three criteria cannot simultaneously be satisfied (Kleinberg et al, 2016) (c.f. Arrow’s Impossibility Theorem). This suggests that the ProPublica investigation is to some extent logically questionable, since the main criticism of COMPAS levelled therein is that it does not meet a similar set of criteria – which may, in fact, be a logical necessity.


*Further developments*

Although most applications of this type of software has been on the far side of the Atlantic, one Cambridge academic in particular is making progress on a similar algorithm. The HART algorithm, masterminded by the Cambridge lecturer Dr Geoffrey Barnes in conjunction with Durham Constabulary, uses random-forest machine learning to perform a broadly similar role – in this case determining whether or not to release prisoners on bail – although the details of the implementation have not been released.. In predicting recidivism it reached an accuracy of 62.8% on its first validation (Oswald et al., 2018). It has lately been put into practice, though it is too soon at present to evaluate its performance. Of course, while it has only been used in limited circumstances, it is sobering to note that COMPAS, also, was never originally intended for sentencing, but instead for determining probation periods (Brennan et al., 2009); HART could similarly end up performing a much more serious role than it was ever intended to. 


*Bibliography*

- Brennan, T., Dieterich, W., & Ehret, B. (2009). Evaluating the Predictive Validity of the Compas Risk and Needs Assessment System. Criminal Justice and Behavior, 36(1), 21–40. https://doi.org/10.1177/0093854808326545

- State of Wisconsin v. Eric L. Loomis, Supreme Court of Wisconsin (2016). Retrieved from https://www.leagle.com/decision/inwico20160713i48 

- Julia Angwin, Jeff Larson, Surya Mattu and Lauren Kirchner (2016). Machine Bias — ProPublica. Retrieved July 8, 2018, from https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing

- Flores, A. W., et al (2016). False Positives, False Negatives, and False Analyses: A Rejoinder to “Machine Bias: There’s Software Used Across the Country to Predict Future Criminals. And it’s Biased Against Blacks”;  Retrieved from http://www.crj.org/assets/2017/07/9_Machine_bias_rejoinder.pdf

- Practitioner’s Guide to COMPAS Core. (2015). Retrieved from https://assets.documentcloud.org/documents/2840784/Practitioner-s-Guide-to-COMPAS-Core.pdf

- Dressel, J., & Farid, H. (2018). The accuracy, fairness, and limits of predicting recidivism. Science Advances. https://doi.org/10.1126/sciadv.aao5580

- Lum, K., & Johndrow, J. E. (2016). A statistical framework for fair predictive algorithms. Retrieved from https://arxiv.org/pdf/1610.08077.pdf

- Kleinberg, J., Mullainathan, S., & Raghavan, M. (2016). Inherent Trade-Offs in the Fair Determination of Risk Scores. Retrieved from http://arxiv.org/abs/1609.05807

- Oswald, M., Grace, J., Urwin, S., & Barnes, G. C. (2018). Algorithmic risk assessment policing models: lessons from the Durham HART model and “Experimental” proportionality. Information & Communications Technology Law, 27(2), 223–250. https://doi.org/10.1080/13600834.2018.1458455org/10.1080/13600834.2018.1458455



