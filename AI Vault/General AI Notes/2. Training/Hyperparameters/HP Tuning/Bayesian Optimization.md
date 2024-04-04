Bayesian optimization is on of the most popular forms of [[Hyperparameter Tuning]]. 

This method trains a set of models, then evaluates them and creates an *acquisition function* which is used to predict the accuracy of the model given a set of hyperparameters.
After this, a new batch of models is trained with hyperparameters which maximize this function.