## Overview
Loss functions create a measurement of how incorrect a network is. Loss basically says "I need to readjust my weights this much." To be more precise, it's a measure of [[Measuring Error|how far away the model is from the data points.]] 

The loss function must be *double differentiable* and *continuous*. Luckily, if something is differentiable, it is also continuous. Making sure this is the case is going to allow us to take the gradient, which is a vector of the  derivatives of a function with respect all variables. Remember that __The gradient shows us the direction a function is going.__ [Video on gradients](https://www.youtube.com/watch?v=DG9NUPaPVbE)

## The Gradient
The gradient is a vector of the partial derivatives of a function. __The derivative of a function $\mathscr{L} (x)$ with respect to a variable $x$ will show us how sensitive the output of the function is with respect to $x$.__ It will also show us *how* $x$ changes our output since it will show us the direction of change.

>[!tip] The gradient shows us how much the parameter $x$ needs to change in order to minimize the function $\mathscr{L} (x)$.

Think about the output of a neural network. Especially with DNNs, this output could be a combination of hundreds of thousands of variables into a binary output function. 

## [[Gradient Descent]]

Let $\theta$ = *every single weight in the network*
$$ \theta_{new} = \theta_{old}  - \epsilon \frac{\partial {\mathscr L}}{\partial \theta_{old}}$$

Where
$\epsilon$ is the learning rate
$\mathscr L$ is the loss function

[[List of Cost & Loss Functions]]
