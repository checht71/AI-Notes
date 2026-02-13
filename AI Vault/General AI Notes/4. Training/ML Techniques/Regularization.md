#overfitting 

## What is it?
TL;DR: Regularization = Generalization

Regularization is basically a penalty as model complexity increases. There are multiple types of regulation, they are all different kinds of functions that penalize complexity in slightly different ways. Regularization essentially lowers the weights.

## Regularization Techniques:

### L1 Regularization:
L1 Regularization is also known as _Lasso Regression_. __L1 adds the sum of the absolute values of the weights to the loss.__ Lasso encourages the weights to approach zero. The weights can even go as low as zero, resulting in a more #sparsely-connected network. This works well for feature selection if there are a large number of features.

### L2 Regularization:
L2 Regularization is designed to be a more nuanced form of regularization than L1.  L2 is also called _Ridge_ or _Weight Decay_.  __L1 adds the sum of the squared values of the weights to the loss.__ This penalizes larger weights much more than smaller ones. The result is a more even distribution of weights, without the amount of sparsity that results from L1. 

### More on L1 & L2:
There is a parameter called _lambda_ in both of these functions. Lambda is a coefficient that you set from 0 to 1 which basically determines how strong the impact each function is on your overall loss. If you set lambda too high, you might accidentally under-fit your model instead of overfitting it.

## [[Dropout]]:
Dropout introduces a probability _p_. This probability is the chance that a neuron will shut off during training and effectively be removed from the network. _p_ ranges from 0 to 1, 0 meaning no neurons are dropped during training and 1 meaning that every neuron will be dropped. This is an important variable that must be determined before training based on how much the model is overfit.

## Early Stopping:
The concept behind early stopping is simple. When we overfit a network, we can often see the loss curve increasing rather than decreasing. Early stopping means we just stop the training process as soon as the loss starts to increase. This is arguably the worst way of stopping overfitting because it stops training when the other methods allow the network to train for more epochs without overfitting as bad.

## [[Data Augmentation]]:
This is a process where images are copied with affects such as random brightness, contrast, rotation, flip, or crop added to them. What this does is it artificially increases the size of a dataset by creating varied versions of images. This is especially helpful for networks which are trained on small datasets.

[Further Reading: Regularization](https://medium.com/towards-data-science/over-fitting-and-regularization-64d16100f45c)
[Further Reading: L1 & L2](https://towardsdatascience.com/l1-and-l2-regularization-methods-ce25e7fc831c)
[Video on Regularization](https://www.youtube.com/watch?v=EehRcPo1M-Q)