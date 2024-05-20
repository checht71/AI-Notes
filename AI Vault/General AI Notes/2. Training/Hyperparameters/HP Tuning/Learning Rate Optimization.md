There are many different ways to optimize learning rate. This section will go over a few that I have come across.

> [!info] A *higher learning rate* usually takes larger optimization steps. This results in the network getting in the ballpark of the loss minimum faster, but has less overall accuracy.

> [!info] A *lower learning rate* takes smaller optimization steps. This results in the network taking longer to get to the correct answer. There's also more noise in the steps, meaning they go in more seemingly random directions. Finally, the steps with a lower learning rate can get stuck in local minima easier and not find the global minimum.

> [!tip] The best overall approach to learning rate is to use *[[Learning Rate Decay]]*. This means that over each epoch the learning rate will start higher and end lower so that it can find the best minimum and then hone in on it. [^1]


Simply picking a learning rate and adding decay will not always provide you with the best results. You can program specific methods the allow the network to learn its own learning rate.

If your loss begins to plateau after a few epochs or goes down very slowly and linearly, try and increase your learning rate.
If your loss becomes sporadic and jumpy, try and decrease it.

[^1]: https://medium.com/analytics-vidhya/learning-rate-decay-and-methods-in-deep-learning-2cee564f910b