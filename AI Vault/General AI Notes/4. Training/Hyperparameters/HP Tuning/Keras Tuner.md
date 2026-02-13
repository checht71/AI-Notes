Keras Tuner is one of the simplest and most intuitive ways to perform [[Hyperparameter Tuning]] in TensorFlow.

## Basic Tuning


Actually setting up a hyperparameter to tune only takes a single line of code. This is an example of tuning an integer such as the number of neurons in a layer.
###### hp.Int
```python
hp_layer_1 = hp.Int('layer_1', min_value=1, max_value=1000, step=100)
```
This will search between 1 and 1000 in steps of 100.

Other types of hyperparameters you can tune are `hp.Choice`, which will go through an array of choices and `hp.Float` which is good for hyperparameters such as the learning rate. Below is an example of `hp.Choice`.
###### hp.Choice
```python
hp_activation = hp.Choice('activation', values=['relu', 'tanh'])
```

In order to use these, we have to pass them into the model in the place where we would usually define the hyperparameter.

```python
hp_layer_1 = hp.Int('layer_1', min_value=1, max_value=1000, step=100)
hp_activation = hp.Choice('activation', values=['relu', 'tanh'])
model.add(tf.keras.layers.Dense(units=hp_layer_1, activation=hp_activation))
```

In order to tune your model, you want to define it and compile it inside of a function so that it can be called by the tuner itself:
```python
def model_builder(hp):

	model = tf.keras.Sequential()

	hp_layer_1 = hp.Int('layer_1', min_value=1, max_value=1000, step=100)
	hp_layer_2 = hp.Int('layer_2', min_value=1, max_value=1000, step=100)
	model.add(tf.keras.layers.Dense(units=hp_layer_1,
					   activation='relu'))
	
	model.add(tf.keras.layers.Dense(units=hp_layer_2, 
						activation='relu'))
	
	model.add(tf.keras.layers.Dense(10, activation='softmax'))
	
	  
	
	model.compile(optimizer=tf.keras.optimizers.Adam(learning_rate=0.01),
	loss=tf.keras.losses.SparseCategoricalCrossentropy(),
	metrics=['accuracy'])
	
	return model
```


After this, we want to set up the tuner outside the function.
```python
import keras_tuner as kt

tuner = kt.Hyperband(model_builder, objective='val_accuracy', max_epochs=10, factor=3, directory='dir', project_name='mnist')
stop_early = tf.keras.callbacks.EarlyStopping(monitor='val_loss', patience=3)
```
This tells the tuner that is going to use the `model_builder` function we defined earlier, train each model for a maximum of 10 epochs (less if the model sucks) and use validation accuracy to assess the models' performance.
We also implement a [[Callbacks|callback]] for early stopping. This will stop the training process for a model if the validation loss does not improve after `3` epochs.


Next we are going to run the tuner. We give it the dataset, the amount of total epochs we want it to run for across all models, as well as other parameters that we would use for training any other model.

```python
tuner.search(X_train, y_train, epochs=20, batch_size=200, validation_split=0.2, callbacks=[stop_early])
```


## HyperModels
A hypermodel is a model that can add and remove its own layers as part of the tuning process. The process of creating a hypermodel is actually pretty straightforward in Keras Tuner. All we have to do is utilize `hp.Int` and a for loop.

```python
number_of_layers = hp.Int('layer_amt', min_value=1, max_value=4, step=1)
for layer_num in range(number_of_layers):
	model.add(tf.keras.layers.Dense(units=64, 
							activation='relu'))
```

This will tune the for loop to add `layer_num` amount of layers to the model. This should be placed within your `model_build` function just like the other layers of the model.