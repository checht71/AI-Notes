Essential skill for some [[Data Engineer]] jobs.

>[!tip] The mindset of Data Pipelining is *how do I make this data easier to work with LATER on down the line as opposed to right now*.






[Check out this video](https://www.youtube.com/watch?v=4WNz2xrGe8w)

### Data Pipelining for Tensorflow
There are multiple ways to make a dataset.

One of the most efficient ways to do data pipelining in TensorFlow is with the TF.Dataset class. Many pipelines simply use numpy arrays to keep track of their images and class labels, but the dataset class will make it much more efficient.


#### Create a dataset from tensor slices
```python
inputs = some tensors: images, lists, arrays, etc.
outputs = labels
tf.data.Dataset.from_tensor_slices((inputs, outputs))
```

Usually you pass in the inputs and outputs (usually called x_train and y_train) as a tuple (not mandatory).


#### Use TF friendly formats
using `tf.data.Dataset.from_tensor_slices()` will put your data and labels into tensor format. If we want to normalize them or edit the data while it is stored as a tensor, we do not convert it back to numpy arrays. That would kind of defeat the purpose. To get around this, we use `tf.cast(data, format)` so that we can edit the info while it is inside the tensor.

#### .map()
Calling `your_dataset_here.map()` will transform the elements in an array based on a function that you have written. 

>[!tip] Make sure that your function returns a tuple of both images and labels. This makes it easy to map dataset objects without adding extra lines of code.


```python
def normalize(images, labels):
	return (tf.cast(image, tf.float32)/255.0, label)

my_dataset = my_dataset.map(normalize, num_parallel_calls=tf.data.AUTOTUNE)

```
	Note: tf.data.AUTOTUNE is boilerplate code. It will make tensorflow automatically determine what the images and labels are in the function.


