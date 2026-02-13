"Exploding gradients are a problem when large error gradients accumulate and result in very large updates to neural network model weights during training. 
Gradients are used during training to update the network weights, but when the typically this process works best when these updates are small and controlled. 
When the magnitudes of the gradients accumulate,  an unstable network is likely to occur, which can cause poor prediction results or even a model that reports nothing useful what so ever."[^1]

TL;DR: Exploding Gradients means that the gradient gets stupidly big and throws off the whole network.

[^1]: https://deepai.org/machine-learning-glossary-and-terms/exploding-gradient-problem