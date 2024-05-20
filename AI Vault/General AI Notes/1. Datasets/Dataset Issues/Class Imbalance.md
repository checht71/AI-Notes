Class imbalance is when there are far more examples of one class in a dataset than another.
## Oversampling and Undersampling
#### Oversampling
Oversampling is when you add fake data points to artificially increase the amount of examples of the less populated class. This is usually done by taking the average of all the existing data points in the less populated and creating new datapoints at the average.

#### Undersampling
Removing data from the more populated class so that it matches with the lesser class.


### Class Weights
This will adjust the learning rate of the network. An example which falls into the more populated class will nudge the gradient descent less than an example which falls into the lesser class.