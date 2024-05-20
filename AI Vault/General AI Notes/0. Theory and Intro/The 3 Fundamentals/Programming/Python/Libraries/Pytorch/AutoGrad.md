Autograd is a way to calculate [[Gradient|gradients]]. Gradients are necessary for [[Backpropagation]]. If you create a tensor and include the argument `requires_grad=True`, PyTorch will automatically compute the gradient every time you do something to that tensor. The gradient can then be called using `tensor.grad()`
`tensor.backward()` is a function which also calculates the gradient.
	The vector Jacobian is used to compute the gradients. This is the vector equivalent of the chain rule from calculus.

If you no longer wish to compute a gradient for a function, you can use `tensor.requires_grad_(False)` or in the case of an optimizer `optimizer.zero_grad`.
