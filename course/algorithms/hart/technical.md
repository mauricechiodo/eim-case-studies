---
Title: The HART Algorithm
Template: LeafPage
---

# The HART Algorithm and Random Forests
$\newcommand{\F}[1]{^{[\text{F}#1]}}$$\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}$$\newcommand{\c}[1]{^{[#1]}}$$\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$

Let

* $\mathcal{O}=${'High-risk','Medium-risk','Low-risk'} be the outputs of HART
* $\mathbb{I}=\prod_{i=1}^{34} I_i$ be the space of all inputs, with each $I_i$ being an input

In most cases, $I_i\simeq\mathbb{N}$ (eg for age), $I_i\simeq${$0,1$} (eg for gender or booleans) or $I_i\simeq[n]$ for some $n$ (eg with ```CustodyPostcodeOutwardTop24```)$\F{1}$
 
Then a random forest $\mathbb{T}$ is a set of $n\F{2}$ 'classification and regression decision trees'$\C{3}{228}$ (hereon 'trees'). These trees $T_i\in\mathbb{T}$ are each an algorithm in their own right that is designed to classify suspects. Or equivalently,  $T_i$ are functions $T_i:\mathbb{I}\to\mathcal{O}$.

The model then decides the output risk,$R$, of a suspect $\bf{I}\in\mathbb{I}$ as being

$$R=\max_{o\in\mathcal{O}}\left(\left|\{T\in\mathbb{T}:T({\bf I})=o\}\right|\right)$$

ie each of the trees vote on which category the suspect should be classed in and the first past the post winner is taken as the output.

## Generating trees

There are 34 predictors used in HART$\F{3}$ that trees can use to predict the categorisation of a suspect. The trees are based on the designs in Berk et al 2016$\c{1}$ which describe the tree creation process as being

1. From the set of training data $D$ of size $|D|=N$, take $N$ samples **with replacement**. Call this sample $S$. Let $S^\complement=D\backslash S$
2. Take a random sample **without replacement** of the predictors of known size (eg 5), call this set $P\subseteq \mathbb{I}$
3. Construct the first branch of the tree using some generation process that takes $S$ and $P$ as inputs. This process will be elaborated on.
4. GOTO step 2 for each branch generated until the tree is as large as desired (usually until all inputs have been incorporated or until the tree has categorised all its training data).
5. Test the tree $T_i$ with the testing data $S^\complement$.
6. Repeat steps 1-5 a large number of times.$\F{2}$

To predict the accuracy of the random forest, for each $d\in D$, take the set of trees that were not trained with it as an input and take a vote over those trees as to its category. Then, statistically identify the accuracy using your favourite method and these predictions of their category versus their known actual category.

## Generating branches

To generate a branch of a tree,$\F{4}$ several concepts need to be introduced.

$$\text{Entropy}(S)=-p\_\oplus\log\_2(p\_\oplus)-p\_\ominus\log\_2(p\_\ominus)$$

Where $S$ is some collection containing positive and negative examples of something (such as if someone does or does not recidivate). $p\_\oplus$ represents the proportion of positive examples, and $p\_\ominus=1-p\_\oplus$. This is a measure of *uncertainty* about your data. $\text{Entropy}(S)\in[0,1]$ is maximised ($=1$) when $p\_\oplus=0.5$ and minimized ($=0$) when $p\_\oplus\in\{0,1\}$.

The information gain ($\text{Gain}(S,A)$) represents the expected reduction in entropy given a certain input used to categorise the data, $A$. The input that minimises entropy will be the one chosen to represent the branch in question of the tree.

$$\text{Gain}(S,A)=\underbrace{\text{Entropy}(S)}\_3-\underbrace{\sum\_{v\in\text{values}(A)}\left(\frac{|S\_v|}{|S|}\centerdot\text{Entropy}(S\_v)\right)}\_{\text{Relative entropy of }S}$$

Where

* $S$ is the set of training data used on the branch
* $S_v$ is the set of training data with attribute $v$

When creating a branch, out of the inputs chosen from the sample, the best will be used in order to categorise the training data selected.

Combining all these processes, you can grow your random forest and have an AI that will categorise certain datasets.

---

# Footnotes

$\F{1}$ ```CustodyPostcodeOutwardTop24``` is "The 25 most common 'outward' (first 3-4 characters) postcodes in County Durham. If the offenders postcode is outside of County Durham".$\C{2}{97}$

$\F{2}$ HART takes $n=509$.$\C{2}{7}$

$\F{3}$ Of which 29 are directly related to criminal history.

$\F{4}$ For classifying a set into *two* classes. The algorithm can be extended to more than two classes.

---

# Bibiliography

$\c{1}$ Berk, Richard A., Susan B. Sorenson, and Geoffrey C. Barnes. “Forecasting Domestic Violence: A Machine Learning Approach to Help Inform Arraignment Decisions.” Journal of Empirical Legal Studies 13, no. 1 (March 2018): 94–115. https://doi.org/10.1111/jels.12098.

$\c{2}$ Urwin, Sheena. “Algorithm Forecasting of Offender Dangerousness for Police Custody Officers: An Assessment of Accuracy for the Durham Constabulary Model,” December 2016, 136.

$\c{3}$ Oswald, Marion, Jamie Grace, Sheena Urwin, and Geoffrey C. Barnes. “Algorithmic Risk Assessment Policing Models: Lessons from the Durham HART Model and ‘Experimental’ Proportionality.” Information & Communications Technology Law 27, no. 2 (May 4, 2018): 223–50. https://doi.org/10.1080/13600834.2018.1458455.
