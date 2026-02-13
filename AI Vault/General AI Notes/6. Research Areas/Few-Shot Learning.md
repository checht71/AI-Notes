Few shot learning is a practice in which an AI model is trained only using a few examples. This is an important field of research, as many important tasks in fields such as medicine have datasets with only a few samples per class. This type of learning is especially prone to [[Overfitting]].

The main technique used in few shot learning is [[Meta-Learning]], or teaching a model how to learn so that it can obtain a better understanding from a few images.

## FSL Dataset Structure
Few shot learning has a *base dataset* and a *novel dataset*. The base (training) dataset is what the model is trained on. It is usually generalized across a wide range of classes or even tasks. The novel dataset is used to test the model. It usually has classes not seen in the novel dataset. In some cases, the two have completely different classes.

In addition, the novel dataset can be broken down into its own training and test set. This is similar to [[Transfer Learning]] where you take an existing model and train/test it on your own dataset. The terms for the novel training and test set are the *support set* and the *query set* respectively.

>[!tip] Dataset Terminology
>Base - generalized tasks used to make an adaptable base model
>Novel - use case dataset. Split into support & query set
>Support - novel training set
>Query - novel test set


The base dataset teaches the model to **learn how to learn**. [^1]

During training on the base set, the model learns to tell the differences and similarities between certain objects. It recognizes features.

>[!tip] More Terminology
>*$k$-way* means the support set has $k$ classes. 
>*$n$-shot* means there are *n* examples of a class in the support set
>increasing $n$ and decreasing $k$ improves  the accuracy of the model.

# Feature Embedding
A *feature embedding* is a numerical representation of data. These values take the form of vectors. The data that passes through the flattening layer of a [[Convolutional Networks|CNN]] is considered to be a feature embedding/vector. The feature space is the bounds in which all of these feature embeddings lie. Low dimensional feature spaces can literally be plotted on a graph[^2]. The key difference between a normal classifier and a meta-learner is in the final layers. Rather than probabilistically comparing the feature vector to learned class representations, the meta-learner directly compares the distance between feature vectors.
# Similarity Function
In order to compare and contrast the examples we have in our feature space with examples from the query set, we need a math function. This function is called the similarity function. In some cases this function is literally another machine learning algorithm. [[K-Nearest Neighbor (KNN)]] algorithms can be used to compare the location of embeddings in the feature space.


### Citations
[^1]: [Few-Shot Learning (1/3): Basic Concepts, Shusen Wang](https://www.youtube.com/watch?v=hE7eGew4eeg)
[^2]: [The Biggest Misconception about Embeddings](https://www.youtube.com/watch?v=ulD7IsecPbU)

### Tags:
#feature-embeddings