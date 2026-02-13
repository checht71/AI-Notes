Inherent explanability is one of the two forms of [[Explainable Models Overview|XAI]], the other being [[Robust Explainability (Paper)|post-hoc explanability]]. Inherent explainability is also sometimes called transparency.

Inherent explainability is when the model architecture is built to be transparent. There are only certain model architectures that work with this.

Examples of models that are built to be inherently explainable are linear models, KNNs, logistic regression models and decision trees. Linear models are explainable because you can chart the data-points and clearly see on a graph the line that the model creates to separate the categories.

## Some Inherently Explainable Models
### Decision Trees
A decision tree is such a simple algorithm that it did not even occur to me that it was AI until someone explained to me that it was. A decision tree is basically just a flow chart that a program follows down. 

Below is an actual decision tree.
![|600](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fmiro.medium.com%2Fmax%2F1280%2F0*4QE-0kavxXfzF_bR.png&f=1&nofb=1&ipt=2f82d644738e4cdf7609ab744bce6f20c2214e01c46601e1d01c528f6204c7c8&ipo=images)

#### Taylor Series
The [[Taylor Series]] is a mathematical concept that you can actually build a machine learning model out of for some applications. They Taylor series is just a one dimensional weighted sum. It will closely approximate a function around a specific point. At their core, machine learning algorithms are just these types of approximates.
[Paper on designing inherently explainable AI](https://arxiv.org/pdf/2111.01743.pdf)