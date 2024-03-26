[Link](https://deepai.org/machine-learning-glossary-and-terms/hyperparameter)

Hyperparameter tuning is one of the most complicated concepts within the field of artificial intelligence.
There are tons of [[Hyperparameter Types]], and the more you want to tune the more computational power you have to throw at your network. Ultimately it's up to you to decide which hyperparameters you want to tune and how much you want to tune them.

## Tuning Methods
### [Grid Search](https://medium.com/fintechexplained/what-is-grid-search-c01fe886ef0a):
Grid search is the most basic form of searching. You literally just train a model with each and every combination of hyperparameters. This is incredibly computationally expensive. The image below is an example of this with only 2 hyperparameters. Notice how in order to train just these two you have to train 20 models.
![[Pasted image 20240321141439.png|500]]
### Random Search:
Random search is just grid search with a shortcut. Instead of sequentially going through every single configuration, pick a few random configurations which are spaced out on the matrix and train those. Out of the first batch, choose 1 or 2 with the highest accuracy, then train the rest of your models around those.
![[Pasted image 20240321141925.png|500]]

### Bayesian Optimization
Bayesian optimization is an approach which creates a probabilistic model of the cost given some sets of hyperparameters. Basically what it does is it takes the first batch of random models from random search and predicts based on that which models will be the most accurate. It will predict the orange cost map shown above in figure 2. Then it will train the models which it predicts have the lowest cost.

[Video: A Review of Hyperparameter Tuning Techniques for Neural Networks](https://www.youtube.com/watch?v=5Xh9FusE8iE)