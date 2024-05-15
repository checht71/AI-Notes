>[!tldr]
>Autograd is a method in PyTorch to *Auto*matically compute the *Grad*ients.


### What's a Gradient?
A gradient is the *slope* of a line or a shape. In simple cases such as a line, the gradient is just the rise over run. In more complicated cases, it is the partial derivative. 

#### Case 1: Rise/Run

#### Case 2: Derivative
Here's a simple derivative from Calculus 1 to refresh your memory. A derivative tells us the rate of change of a function, or how quickly the function is changing.
$$
y = x^2
$$
$$
\frac{dy}{dx} = 2x
$$
#### Case 3: Full Gradient
While the first two examples technically fit the definition of a gradient, this definition is typically what we actually mean when we say gradient.
The gradient is something introduced in multi-variable calculus (Calculus 3). It takes the partial derivative with respect to every variable. The output of this function is a vector containing the rate of change with respect to each variable.

$$\nabla f = \frac{\partial f}{\partial x} \hat{i} + \frac{\partial f}{\partial y} \hat{j} + \frac{\partial f}{\partial z} \hat{k}$$


This does not only work for equations with 3 variables, the gradient applies to any equation with 2 or more variables. Just add or remove a partial 
