---
Title: Bias
Template: ListSubPages
---



# Bias
On April 1st 2018, a group at MIT created an 'AI-powered psychopath' named Norman [1]. Norman is a machine learning algorithm trained 
or image captioning. The idea is that Norman is shown an image, and it will give a caption to accompany the image. For a traditional
image captioning algorithm, the output would ideally describe what the image contains. However, Norman was trained on "image captions
from an infamous subreddit (the name is redacted due to its graphic content) that is dedicated to document and observe the disturbing
reality of death." Then, Norman's responses to being shown randomly generated images of inkblots were compared with a standard image
captioning neural network. Unsurprisingly, despite the variety of responses of the standard image captioning neural network output,
Norman saw people dying in every image. While this is an extreme example, this does demonstrate that the data that machine learning
algorithms 'learn' from has a big affect on the output. Therefore, if the data input into decision making algorithms are biased, the
decisions that the algorithm makes will be biased. This is important to consider when using historical data because society has
historically been bias and therefore using historical data can result in bias in the algorithm, embedding the bias into the future. Even if
the data isn't explicitly bias, implicit bias can exist and emerge through the use of machine learning. For example, Durham Police recently
removed a 'postcode' field in the data submitted to their HART algorithm [2, p.21] because of fears it would discriminate against poorer people.

Whilst data is a major source of bias in machine learning algorithms, it is not the only source of bias. The UK Government's Science and
Technology Committee [2, p.19] recognised this and recommend sufficient diversity on algorithm development teams to help reduce intrinsic bias
built into an algorithm. Even though the machine learning algorithm chooses the value of parameters to help make the 'best' decision,
humans choose the goals that the algorithm aims to achieve. Moreover, algorithmic development teams also decide on what data the algorithm
is shown, reducing bias in the development team can potentially lead to a reduction in bias through the training data the algorithm is
given. Related to this is a suggestion made in that technical people working on AI algorithms are not sufficiently trained in ethics to
deal with the Analysing the fairness of an algorithm is also a contentious topic. As part of this Ethics in Mathematics Series, there has
been some discussion on this topic. The section [Fairness and Decision Making](/course/course/algorithms) has
more details about this. 

### References

[1] [Norman, by MIT Media Lab](http://norman-ai.mit.edu)

[2] [Algorithms in decision-making](https://publications.parliament.uk/pa/cm201719/cmselect/cmsctech/351/351.pdf) *UK Science and Technology Committee - Ordered by the House of Commons*
