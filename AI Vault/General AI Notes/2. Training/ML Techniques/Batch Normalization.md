> [!abstract] TL;DR
> Batch Normalization makes your data more AI friendly by scaling it between 0 and 1. 

Batch normalization centers and stabilizes feature maps.

Normalization is just putting our data on a widely known or standard scale (in most cases from 0 to 1). Large outliers in datasets can cascade through the layers in the network and cause problems, such as the [[Exploding Gradient]] Problem.

### Benefits of Batch Normalization
- Deals with exploding gradient problem
- Makes network train faster
- Can help ease overfitting
- Reduces the need for [[Regularization]]

>[!Example] Example:
For example, if I had 2 metrics for my inputs: miles driven and age, miles driven can range from 0 to 100,000, and age can range from 0 to 100. These are two widely different numbers are fed into the network at the same time. This can result in the weights of the neural network varying widely, creating an unbalanced network. To mitigate this, we just squish the metrics down to range from 0 to 1 for both metrics, so they are the "same" in the network's eyes.

#### Application:
Batch normalization is only applied to layers that you choose to apply it to. It will normalize the outputs from the activation functions. Another interesting thing to note is how the data is scaled will be learned like any other parameter such as the weights during training.

Batch normalization can be added using Keras.
All you have to do is go to the layers of your sequential network and put `BatchNormalization(axis=0)`  after the layer you would like to normalize.

```python
model = keras.Sequential(    [        
layers.Dense(2, activation="relu"),
BatchNormalization(axis=0),
layers.Dense(3, activation="relu"),
layers.Dense(4, name="layer3"),
])
```

The authors of the batch normalization also spoke favorably about having batch normalization before the activation function. This can be done by having the activation function as its own layer instead of being an argument of the dense layers.

```python
model = keras.Sequential(    [        
layers.Dense(2),
BatchNormalization(axis=0),
layers.Activation("relu")
layers.Dense(3),
BatchNormalization(axis=0),
layers.Activation("relu")
layers.Dense(4, name="layer3"),
])
```

[Source 1](https://arxiv.org/pdf/2209.14778.pdf)
[Source 2](https://deepai.org/machine-learning-glossary-and-terms/batch-normalization)
[Source 3](https://www.youtube.com/watch?v=dXB-KQYkzNU)
[Source 4](https://www.youtube.com/watch?v=yXOMHOpbon8)



[Using Normalization Layers to Improve Deep Learning Models](https://machinelearningmastery.com/using-normalization-layers-to-improve-deep-learning-models/)
[How to Normalize, Center, and Standardize Image Pixels in Keras](https://machinelearningmastery.com/how-to-normalize-center-and-standardize-images-with-the-imagedatagenerator-in-keras/)