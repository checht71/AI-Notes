[Article](https://www.baeldung.com/cs/mini-batch-vs-single-batch-training-data)

## Mini-Batches vs Batches
The batch size that I am currently using on my laptop (3) is considered a mini batch size. More commonly used batch sizes are 32, 64, 128, 256, etc. My batch size uses less RAM and updates the model more frequently at the cost of speed when training. It's also good because we reduce the risk of getting stuck at a local minimum.

![[Pasted image 20230227113224.png]]

## Stochastic Gradient Descent (Super Mini Batches)
In a sentence, stochastic gradient descent is when you have a batch size of 1. That means the network is updated after every single image/sample you train on. This model is noisy, especially when you have data with a high amount of variance. If one sample points one way and another with the same label points another, your loss function is going to be off the charts.
![[batchsizelossexample 1.png]]
Here's an example of stochastic vs mini batch size. Both arrows point towards the same dot, but they both point in vastly different directions. If we have a batch size of 2, we can merge them together into a single gradient which still points in the same direction (the blue dot). They will both essentially do the same thing if executed perfectly, but in practice it is much easier for the AI to chase 1 gradient in one direction than 2 in different directions. This also means that "the model can jump around, having different variances at different epochs".

[[Gradient Descent|More on stochastic gradient descent]]


[[Batch Sizes and Running Out of Memory]]