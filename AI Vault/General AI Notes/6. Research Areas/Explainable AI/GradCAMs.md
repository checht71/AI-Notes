A GradCAM is uses the weights and biases of the network to create a heat map which it then overlays on top of an image. This shows you what parts of the image the model is focusing on it make its prediction and what parts of the image it thinks are irrelevant.
![[GradCAM.png]]
Here's an example of a GradCAM. Since the red is on top of the parts of the image containing the object that we want to classify, we know that the model is focusing on the right parts of the image.
