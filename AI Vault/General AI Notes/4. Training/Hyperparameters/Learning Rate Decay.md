[[Learning Rate Optimization]] is an interesting problem within the realm of neural networks. Learning rates are part of [[Gradient Descent]] A learning rate that is too high may lead the network to over correct and bounce around the optimal loss, much like a basketball that circles around the net but never goes in.

![600](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*0H7_exu-hFDwXJe9LBzW0A.png)
Figure 1: An example of a high learning rate. Notice how noisy the line is. It's all over the place and never settles at the optimal location (the center).

On the other hand, a learning rate that is too low can become stuck in local minima/maxima. These are pockets of loss that seem like they yield the highest accuracy when you look directly next to them, but if you were to look at the bigger picture you would see that there are clearly see that there are better configurations that you could arrive at.

![600](https://velog.velcdn.com/images/cha-suyeon/post/fbd6c3d9-a033-4870-8bff-a3f9a0727fe3/image.png)
Figure 2: An example of a local minima vs a global minima. An [[Optimizers|optimizer]] with a low learning rate is much more likely to get stuck in a local minima.

### Learning Rate Decay Functions
There are many different ways of creating a learning rate decay function. Really any function with a negative slope can qualify as one of these functions, but there are some that are more widely used than others. Selecting the best function can yield performance benefits for your network in terms of accuracy or training time.

>[!tip] In order to implement a learning rate decay function, you must use a [[Callbacks|callback]] so that the learning rate changes at each epoch.

Let's define some variables for the following equations:
Learning rate = $\alpha$
Initial learning rate = $\alpha_0$
Decay rate = $d$
Epoch = $e$

#### Function 1: Linear Decay
This is the most common form of learning rate decay. For most use case scenarios, it's best to start with this one.
$$\alpha = (\frac{1}{1+d\times e})*\alpha_0$$

#### Function 2: Exponential Decay
This is an exponential form of the linear decay seen previously. For this to work, $d$ must be less than 1.
$$ \alpha = d^e \times \alpha_0$$

#### Function 3: Discrete Staircase
$$\alpha = \alpha_0 - d\times t$$
The main difference between this function and something like linear decay is that this function is time based rather than epoch based.


#### Function 4: Epoch Based
$$\alpha =\alpha_0 \frac{k}{\sqrt{e}}$$

#### Function 5: Mini-Batch Based
$$\alpha =\alpha_0 \frac{k}{\sqrt{m}}$$
This is the same function as the epoch based function, however it is dependent on the variable $m$, which represents the [[Batch Sizes|mini-batch]] number. 



## Implementation:
### TensorFlow:
You can implement learning rate decay using `tf.keras.optimizers.schedules.ExponentialDecay`. There's also cosine decay, polynomial decay, linear decay, etc.

To implement this, you call it and then pass it into your optimizer:
```python
initial_learning_rate = 0.1
lr_schedule = keras.optimizers.schedules.ExponentialDecay(
    initial_learning_rate,
    decay_steps=100000,
    decay_rate=0.96,
    staircase=True)

model.compile(optimizer=keras.optimizers.SGD(learning_rate=lr_schedule),
              loss='sparse_categorical_crossentropy',
              metrics=['accuracy'])

model.fit(data, labels, epochs=5)
```

[Source](https://www.tensorflow.org/api_docs/python/tf/keras/optimizers/schedules/ExponentialDecay)

### PyTorch:
In order to use a learning rate scheduler in PyTorch, you need to call the scheduler and pass the optimizer into it.
```python
optimizer = torch.optim.Adam(model.parameters(), lr=0.01)
scheduler = torch.optim.lr_scheduler.ExponentialLR(optimizer=optimizer, gamma=0.1, last_epoch=-1, verbose='deprecated')
```

After that, you need to call `scheduler.step()` after every training loop. Here's so psudeocode.

```python
for epoch in range(epochs):
	train_one_epoch()
	sheduler.step() # < update lr
	validation_step()
```