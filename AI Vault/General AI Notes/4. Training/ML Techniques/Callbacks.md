A callback is a function that you pass into another function the same way that you would pass in a variable. This essentially passes tasks directly from one function to another rather than going back to the top level code.

```python
def plotgraph(x):
	plt.plot(x)

def euclidean(numbers, callback):
	x = numbers + 1
	callback(x)

euclidean([1,2,3], plotgraph)
```

[Here's a simple video explaining the idea behind callbacks](https://www.youtube.com/watch?v=-mir74x3f5Y)

## Callbacks in Keras
Think about your normal training loop in Keras. Generally you call `model.fit` and you wait until the model is trained to do anything. But what if I want to perform a specific action at every epoch or every batch? Well, we have to put other functions *within* our `model.fit` function, AKA *callbacks*.

##### Weights and Biases Callbacks
Weights and biases is considered a callback because it *[[Weights and Biases Logging|logs]]* [[Model Evaluation|evaluation metrics]] such as accuracy, recall, precision, loss, etc. at the end of every epoch.