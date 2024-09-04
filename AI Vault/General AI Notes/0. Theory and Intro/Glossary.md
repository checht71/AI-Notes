Convolutional-Neural-Network (CNN): A neural network which has additional 'convolutional' layers which take the input (usually an image) and create a simpler, easier to process version of it in which the features stand out. Think of down-scaling an image in Photoshop.

tensor: a tensor is a multidimensional representation of an image. It is basically the 3+ dimensional version of a matrix. It is used to store information about the features of an image.

Kernels: A filter in a convolutional layer, designed to make certain features from the data stand out for prediction.

SoftMax Function: The softmax function is generally the last activation function before the output. It is what creates the probability distribution.

Bayes-Theorem: predicts the probability of an event based on our prior knowledge of conditions that might be related to the event.

Bayesian-Inference: Using Bayes' Theorem to update the probability of a hypothesis as more evidence or information becomes available.

Posterior-Probability: an updated probability, specifically updated using Bayesian Inference.


Probability-Distribution: An array of values representing the likelihood of a possible answer being true.

Posterior-Probability: an updated probability, specifically updated using Bayesian Inference.

ReLU: Rectified Linear Unit Activation Function. A piecewise linear function that will basically just only output positive values as they are. If an incoming number is negative, it will output 0. This is more simple and more effective than the sigmoid function.

Variability: How far data points lie from each other and from the center of a distribution. A measure of how far apart points are.

Covariance: A measure of the relationship between two random variables. Shows if they are 'moving in the same direction'. The best example of covariance is in finance. Assets like stocks and ETFs have a high covariance because they behave the same way under the same kind of market conditiw-shot dataset generalization is a challenging variant of the well-studied few-shot classification problem where a diverse trainons. Assets like bonds and stocks have low covariance because they tend to behave a little bit differently under the same market conditions.

Covariance-Matrix: A type of matrix which represents covariance between pairs of elements. Also called a "variance covariance matrix". It is always a square matrix. Covariance is represented by a number that that is repeated in a diagonal line across the matrix and variance is all of the other elements in the matrix.

Adversarial-Attack: A type of attack on a neural network where noise is added to the data so that the network makes the wrong prediction. Prevents neural networks from being used in miliary, medical settings.

Gaussian-Distribution: Also called a normal distribution. It is a distribution that is symmetrical at its average. A bell curve is one example.

Gaussian-Function: The function that forms the bell curve of the Gaussian Distribution.

A-posteriori: Emprical reasoning, going from specific facts or particulars to a larger, more general conclusion.

Variational-Inference: A way to get a probability function which produces your current results. We are looking for the possible prior and likelihood just from the posterior. It is essentially a way to "solve", or at least get an approximation of, Bayes' theorem in reverse.

Intractable: a fancy way for saying unmanageable, Incredibly hard if not impossible to solve. Usually used when referring to an equation.

ELBO: #Evidence-Lower-Bound: Takes an intractable inference problem and transforms it into an opimization problem which can be solved using the gradient (multidimensional derivative.)

Loss-Function: function which compares the prediction of the network and the expected value and returns a value which represents how innaccurate the data is based on the current weight configuration. Lower loss = more accuracy. 

Gradient: I learned this in calc 3. It is a 3D slope/derivative. It can also be in higher dimensions. 

Automatic-Differentaton:

Variational-Density-Propagation (VDP): 

Unscented-Transformation (UT): A way to estimate a nonlinear transformation, particularly of a distribution. This is what uses sigma-points. Sigma points are a way to 

sigma-points:

Resnet: A RESidual NEural neTwork.

first-order-approximation: Has something to do with taylor series

TND, tensor-Normal-Distribution: A normal distribution is a Gaussian-Distribution. A tensor normal distribution is a tensor whose values follow this kind of curve.

non-linearities: any output which has a non linear realitionship to an input

variational-distribution: 

Extended-variational-density-propagation: Using a Taylor Series to approximate the mean and convariance of our #Probability-Distribution at each layer of the network. We do this most likely because the activation function is non-linear and would make actually doing the math to precisely adjust the distribution #intractable.

feature-maps: also called an activation map. A feature map is a filtered version of an input image made by kernels which highlights certain features. It is the result of a convolutional operation.

batch-size: how many images a network processes before updating its weights.

Transfer-Learning : the use of a pre trained network on a problem that it was not initially meant to solve.

data-mining: The process of gathering data for supervised learning. This usually involves scraping data from different sources around the web.

[[Backpropagation]]: backpropagation is a learning algorithm used to create a prediction of how much an AI must adjust its weights in order to improve its accuracy.

bonanza : A rich vein of ore; a situation from which large profits are made; or a large amount of something good.

Hebbian-Principle: Neurons that fire together wire together. This is a term that is used in neurology that translates perfectly into neural nets.

regularize: Simplifying an algorithm to have the same amount of loss and accuracy but a more general way of "looking" at data. It's essentially the process of making an AI more general. There are multiple ways to solve the complex optimization problems AI works on. Regularization biases the neural network towards the simplest solution.

ensemble: A technique where multiple neural networks with different architectures are trained and predict on the same data. Their outputs are averaged into one prediction. This is a resource intensive method of lowering overfitting.

[[Dropout]] : A technique in which neurons within a network are randomly  shut off, or "dropped" to simulate different architectures without creating a #ensemble . This technique works better in larger neural networks.

testing-time-augmentation:

mini-batch: a batch, but you only take a subset of your data during one iteration, rather than sampling from the whole thing.

hyperparameter: a parameter which controls the training process.

naive-algorithm: simple, straightforward algorithm. Could be a brute force approach to a problem.

black-box: not [[Inherent Explainability|inherently explainable]]. Needs an additional framework in order to get an understanding of the inner workings.

white-box: [[Inherent Explainability|inherently explainable]].

autograd: A way of computing the gradient. It computes partial derivatives while applying the chain rule.

few-shot-learning: term for AI models learning on only a small number of training data.

feature-effect: the relationship between a feature and the model's output.

RL : Reinforcement Learning.

full-stack: someone who does *both* front-end and back-end work.

artifact: A bit of information from the training process we can use to recreate a model. This can include weights and biases, configuration, preprocessing modules, environment information, etc. This 

feature embeddings: an embedding is a numerical representation of data, usually stored in the form of a vector. [source](https://www.youtube.com/watch?v=ulD7IsecPbU)

feature space: the space on a graph in which the feature embeddings fall.

hypothesis space:

error decomposition: 