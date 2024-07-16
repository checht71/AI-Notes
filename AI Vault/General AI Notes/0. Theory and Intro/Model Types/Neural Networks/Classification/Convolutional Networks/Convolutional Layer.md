An image is based on the idea, that one pixel is dependent on its neighboring pixels, and the next pixel is dependent on its immediate neighboring pixels (be it color, brightness, contrast, and so on). CNN’s work on this idea, and uses filters on a patch of an image to extract important features and edges. This helps the model to learn only the necessary important features from an image, and not details of each pixel of an image.[{1}](https://towardsdatascience.com/are-transformers-better-than-cnns-at-image-recognition-ced60ccc7c8)

### Convolutional Layers in Architecture
As your data passes through the network, it should be identifying more features from the image at a higher level. to accomplish this, the number of output channels should increase with each layer.


### Calculating Outputs of Conv2D Layers
Output Height = ((Input Height - Filter Height + 2 * Padding) / Stride) + 1 
Output Width = ((Input Width - Filter Width + 2 * Padding) / Stride) + 1



### Conv Layer Parameters in PyTorch
[source](https://pytorch.org/docs/stable/generated/torch.nn.Conv2d.html)

`kernel_size`: this is how many elements the convolutional layer will focus on at once. 
`stride`:  adding stride will make the kernel skip `x` pixels as it goes across the image.
`padding`: this adds `x` extra pixels around the border of the image. This is helpful when you need to focus on elements in the borders of images.
`dilation`:


[More info on covolutional parameters](https://d2l.ai/chapter_convolutional-neural-networks/padding-and-strides.html)