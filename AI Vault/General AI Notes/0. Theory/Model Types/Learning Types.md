
TL;DR: Supervised learning uses a labelled dataset. unsupervised learning does not have labels in the dataset; the AI creates categories and sorts them.

![[Pasted image 20230919135642.png]]

## Supervised Learning:
Supervised learning is when you train a model on a labelled dataset. Most of the simpler neural networks programmed in tensorflow have supervised learning. Supervised learning creates networks which fall into one of two categories:

### Classification:
Classification networks take new data and sort it into one of the categories it was trained on. The classic example is images of cats and dogs.

### Regression: 
This type of neural network creates a relationship between a dependent variables and an independent variable. One example would be gross income predictions for the next quarter based on historical sales data. Another example would an assessment of credit risk for a borrower based on a profile created on them.


## Unsupervised Learning
Unsupervised learning is when an algorithm is given an unlabeled set of data and has to create categories for it on its own. Here are some use case examples:

### Clustering:
This kind of algorithm just groups objects together based on their similarities or differences. Ex: K-means

### Association:
This type of algorithm takes individual variables within data and finds relationships between them. An example of this is "Customers who bought this also bought".

### Dimensional Reduction
A type of preprocessing where an algorithm is used to "clean" data, that is, remove extraneous variables while preserving the overall integrity of the dataset. This is supposed to reduce noise and increase quality.


[Further Reading](https://www.ibm.com/cloud/blog/supervised-vs-unsupervised-learning)





#supervised-learning #unsupervised-learning #training #Classification #regression #dimensional-reduction #association #clustering