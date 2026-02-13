Max pooling layers are layers containing compression algorithms typically added after [[Convolutional Layers]]. These algorithms will use a kernel to sift through the layers of a network, pick specific pixels, and create a new image which preserves the features.[^1]

[^1]: https://www.youtube.com/watch?v=ZjM_XQa5s6s


### MaxPool2D Parameters
In PyTorch the 2D maxpooling layer is "maxpool2D".

Parameters:
`kernel_size`: how many pixels are combined into 1.
`stride`:  adding stride will make the kernel skip `x` pixels as it goes across the image.
`padding`: this adds `x` extra pixels around the border of the image. This is helpful when you need to focus on elements in the borders of images.
`dilation`
`return_indicies`
`ceil_mode`


##### Output:
$$
H_{out} = \frac{H_{in} +2*padding-dilation*(kernel\space size -1) - 1}{stride}+1
$$