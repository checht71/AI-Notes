### Overview
Backpropagation is an algorithm that determines how the weights should be updated to meet the desired output of the neural network. This happens from the last layer to the first, hence the name backpropagation. Traditional backpropagation takes the difference between the desired output and the actual output for each class and averages them all out. The resulting number is then added to the weight, readjusting it.

### Batches
Backpropagation is done in batches in order to speed up the training process and reduce computational complexity. #batch-size is considered a hyperparameter which you must fine tune to get the best results. A high batch size generally results in over-generalization and training localizing to local minima, and a low batch size leads to longer training times.
## Backpropagation in Depth
Let $x$ be some tensor.
Let $y = a(x)$ and let $z = b(y)$.

Essentially all we're saying is that $x$ is passed through 2 functions to become $z$. 

We can find the derivative $\frac{dz}{dx}$ using the chain rule.
$$\frac{dz}{dx} = \frac{dz}{dy} * \frac{dy}{dx}$$

We are taking the derivative of both steps and multiplying them together to create the derivative of all operations. This creates a #local-gradient. A local gradient is a gradient of all of a neurons inputs to its outputs.

Now imagine a third and final function: our [[Cost & Loss Functions|loss function]]. In the same way that we can compute $\frac{dz}{dx}$, we can also compute $\frac{dLoss}{dx}$. Since loss measures error, we want this number to be as small as possible.

## The Steps of Backpropagation:
1. Forward pass: apply functions such as $a(x)$ and $b(y)$.
2. Compute the local gradients.
3. Backward pass: compute $\frac{dLoss}{dWeights}$ using chain rule.

## Further Study
#### Videos:
[Overview of Backpropagation](https://www.youtube.com/watch?v=Ilg3gGewQ5U)
[Math Behind Backpropagation](https://www.youtube.com/watch?v=tIeHLnjs5U8)