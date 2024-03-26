#Transfer-Learning 

## Overview
Transfer Learning is a process where you take a pre-trained network, usually one that is adjusted to a very large and broad dataset, and retrain it for a new problem. Transfer learning is best used if you want to train a model on a small dataset.

### Why is this better than retraining a network from scratch?
Good pretrained networks are extremely optimized when it comes to feature extraction. This feature extraction can be used in the new purpose of the network.

### Methods of Feature Transfer
1. Feature Transfer - In feature transfer, the last layer of a pre-trained network is removed, and its previous activation value sent to a classifier. 
2. Parameter Transfer - In parameter transfer, only a few layers of the network need to be reinitialized with the remaining layers using the weight parameters of the pre-trained network and then using the new data set to fine-tune the network parameters. 

Essentially what both methods do is take the major feature extracting parts of the network, utilize those unchanged, and take the last few layers of the network and retrain only those.


## Workflow
The most common incarnation of transfer learning in the context of deep learning is the following workflow:

1. Take layers from a previously trained model.
2. Freeze them, so as to avoid destroying any of the information they contain during future training rounds.
3. Add some new, trainable layers on top of the frozen layers. They will learn to turn the old features into predictions on a new dataset.
4. Train the new layers on your dataset.

A last, optional step, is **fine-tuning**, which consists of unfreezing the entire model you obtained above (or part of it), and re-training it on the new data with a very low learning rate. This can potentially achieve meaningful improvements, by incrementally adapting the pretrained features to the new data.

### How many Layers should I Retrain?
There is no set recommendation for how many layers would work best to retrain a model, but when you're trying it out, you should keep in mind that the beginning layers in a network are used to extract simple features such as lines and curves, and then more complex features such as the outlines of objects are detected by later features. The number of layers you remove should be inversely proportional to how much the pre-trained dataset overlaps with your own dataset. If it seems like the model can extract quite a bit of features of your desired object, not a lot of new layers are needed. If you remove one and there's still trouble, keep stripping the layers away.

## Implementation with Keras
[Transfer Learning Tutorial (Video)](https://www.youtube.com/watch?v=WJZoywOG1cs)
[Keras Transfer Learning Guide](https://www.tensorflow.org/guide/keras/transfer_learning)



#### Sources
[What is Transfer Learning? (Video)](https://www.youtube.com/watch?v=DyPW-994t7w&list=PLcWfeUsAys2nPgh-gYRlexc6xvscdvHqX&index=16)
