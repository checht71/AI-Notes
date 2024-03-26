Convolutional layers are layers of a neural network designed to go over an image and highlight specific features of it so that the dense layers of the network are better able to extract relevant data from each image.

### [Convolutional Filters](https://stackoverflow.com/questions/36243536/what-is-the-number-of-filter-in-cnn)

![[Pasted image 20230209201507.png]]
Convolutional layers create #feature-maps .

Each convolutional layer has a set number of filters. These filters are what detect patterns within the image. With each convolutional layer that an image passes through, the filters get more complex. The first convolutional layers detect basic features of an image such as patterns and the directions of lines, and these patterns turn into more complex encodings which specialize in highlighting specific features in an image such as faces, eyes, noses, wheels, etc.
When you define a convolutional layer in your model it looks like this:
```python
layers.Conv2D(32, 3, padding="same"),
```

32 = the number of neurons in the convolutional layer
3 = indicating 3x3, the number of pixels in the kernel
padding = "same", [padding](https://machinelearningmastery.com/padding-and-stride-for-convolutional-neural-networks/)
