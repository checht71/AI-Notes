[Article] (https://machinelearningmastery.com/dropout-for-regularizing-deep-neural-networks/)
Dropout is a technique in which neurons within a network are randomly  shut off, or "dropped" to simulate different architectures without creating an #ensemble . This technique works better in larger neural networks.

## Connection to Neuroscience
Throughout the history of psychology it has been shown that the brain will rewire itself if it is injured. If someone is blind, their sense of hearing or smell may be better because that part of their brain has been rewired to these organs. Lobotomies typically did not work on children either for this reason: their brains were plastic enough where even though they were missing their frontal lobe they could still retain relatively normal  function due to other portions of their brain being repurposed.
This is the same principle that goes into dropout. If a network is lacking a certain neuron during training, typically another one will be activated and pick up the slack. In practice, dropout is essentially creating a variety of different networks out of very similar architectures.
Dropout will also make training more noisy, which will force a network's loss out of a local minima much like in #Stochastic-Gradient-Descent. 

# Implementing Dropout
Dropout introduces a variable: the _dropout rate __p___ that a neuron will be dropped from the network. _p_ ranges from 0 to 1, 0 meaning no neurons will be dropped, 1 meaning all of them will be dropped. What _p_ is should be determined before training based off of your evaluation of the network. Keep in mind: __all neurons that are dropped during training are added back into the network for testing.__ In order to account for this, we have a _keep probability __k___ that we multiply the inputs by during testing. The equation for k is simple, it is 1 minus the dropout rate.

__k = (1-p)__
