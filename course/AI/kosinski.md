---

Title: Kosinski and Wang

Template: ListSubPages

---


In February 2018, a paper entitled "Deep neural networks can detect sexual orientation from faces" was published in the Journal of Personality and Social Psychology. The authors were Michal Kosinski and Yilun Wang, both associated with Stanford University at the time the paper was written. The pair fed 35,326 facial images into a deep neural network to extract features from them. Then, these features were entered into a logistic regression with the aim of classifying sexual orientation. With just five facial images, the algorithm was accurate in 91% of cases for men, and 83% for women. Human judges had respective accuracies of 61% and 54% according to the study. The implications of this are dangerous. The paper itself recognises that the study performed poses a threat to the safety and privacy of gay men and women.

The testing methodology was, broadly speaking, as follows:

- The images used were self-taken images obtained from online dating websites, the reasons given are that these images can be collected in large numbers, from more representative samples and at a lower cost.

- Face++, a widely used face-detection software, was used to identify the location of the face, outline elements and identify the head orientation. This was used to remove unsuitable images, such as those where there were multiple faces in the picture, or where the person was not directly facing the camera.

- Next they employed Amazon Mechanical Turk (AMT) workers to verify that the faces were adult, Caucasian, fully visible and of a gender that matched the one reported on the user's profile.

- Then some users were randomly removed to balance the age distribution and size of the sexual orientation subsamples.

- Facial features were extracted from the images using a widely employed deep neural network, called VGG-Face. A logistic regression model was trained to classify sexual orientation using 500 singular values extracted from the VGG-Face scores. 

- Finally the model was used to predict the sexual orientation of the participants in a test set.

It is important to note that Kosinski is a psychologist, not a mathematician or a technical trained individual. In the Author's Notes on the paper, Kosinski and Wang stress that they "studied existing facial recognition technologies, already widely used by companies and governments." Technical people were the ones to build these technologies. This study is a clear demonstration that tools created by mathematicians and computer scientists can be used for very ethically unsound purposes by people without technical training. As the ones making this possible, the technicians have a responsibility to think about the potential consequences of their research and the tools created from it. 
