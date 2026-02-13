[Article 1](https://www.pinecone.io/learn/cross-entropy-loss/)
[Article 2](https://365datascience.com/tutorials/machine-learning-tutorials/cross-entropy-loss/)

Cross entropy, like other [[Cost & Loss Functions]], is a measure of how well the neural network fits the data. Cross entropy is generally used in conjunction with a #SoftMax output.
The cross entropy loss finds the difference between two data points.

Cross entropy loss is the most popular loss function in #Classification .


## The Math of Cross-Entropy

Cross entropy much more simple than it seems. All you have to do is take the log of your prediction after softmax, multiply it by the known value of the class, and make that number negative. That's it.

##### Cross-Entropy for 1 Class:
$$-t*ln(y)$$
Where:
$y$ is the predicted variable
$t$ is the #target-variable or known class.

For multiple classes you just take the sum of the cross-entropies for each. This is the most common form you will see in ML.

##### Multi-Class Cross-Entropy
$$Cross~Entropy = L(y,t) = -\sum_{i}^mt_i\;ln(y_i)$$
where:
$m$ is the number of output classes
$i$ is a sample

