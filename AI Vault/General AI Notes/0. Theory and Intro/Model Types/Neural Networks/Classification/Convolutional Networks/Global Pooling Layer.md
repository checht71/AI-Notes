There is an issue in convolutional networks. The amount of filters should increase as an image/data passes through convolutional layers. The last layer usually has hundreds of feature maps. This is an enormous amount of data even after maxpooling, especially if you have a large image.

The Global Pooling Layer is designed to get around this. Global pooling takes each filter and simplifies it down to a single value.

instead of flattening the feature maps, you can use global average pooling 
(`nn.AdaptiveAvgPool2d`) or global max pooling, which reduce each feature map to a single value. This method drastically reduces the number of parameters and computational load in the fully connected layers.


[source](**https://www.youtube.com/watch?v=FUv5NHL9s_U**)