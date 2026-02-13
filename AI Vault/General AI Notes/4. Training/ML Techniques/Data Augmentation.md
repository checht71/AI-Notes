>[!abstract] TL;DR
>Data Augmentation adds copies of images with filters on them to the dataset. The AI can still get valuable info out of these copies for training.

Data augmentation is a unique [[Regularization]] process. Data augmentation creates copies of images from your dataset and applies different effects to them. This artificially makes your dataset larger.

"The artificially expanded training dataset can result in a more skillful model, as often the performance of deep learning models continues to scale in concert with the size of the training dataset. In addition, the modified or augmented versions of the images in the training dataset assist the model in extracting and learning features in a way that is invariant to their position, lighting, and more.[^1]

There are multiple ways to implement data augmentation.

## 1. Testing Time Augmentation (TTA)
This form of data augmentation takes place during testing, hence the name. The images from the testing set are augmented and then the predictions made on them are averaged to produce the final output. This might result in better predictive performance.

#### Implementation of TTA:
The most resource friendly way to implement TTA is to train your model, save it, then load it in with TTA code and have it predict on a small test dataset. This will allow you to test different methods of TTA without retraining the model every time you want to try a new form of it.

#### In TensorFlow
Data augmentation can be done quickly and easily in tensorflow using keras ImageDataGenerator[^2]. Below is an example for the implementation of an augmented training and testing set: 

```python
from tensorflow.keras.preprocessing.image import ImageDataGenerator

train_generator = data_generator.flow_from_directory(DATA_DIR,
target_size=im_shape, shuffle=True, seed=seed,
class_mode='categorical', batch_size=BATCH_SIZE, subset="training")

validation_generator = data_generator.flow_from_directory(DATA_DIR, target_size=im_shape, shuffle=False, seed=seed, class_mode='categorical', batch_size=BATCH_SIZE, subset="validation")
```


[Check out this source to find out more about how to implement testing time augmentation](https://machinelearningmastery.com/how-to-use-test-time-augmentation-to-improve-model-performance-for-image-classification/)


[^1]: https://machinelearningmastery.com/how-to-use-test-time-augmentation-to-improve-model-performance-for-image-classification/
[^2]: https://studymachinelearning.com/keras-imagedatagenerator-with-flow_from_directory/