>[!tip] ### _Good XAI is good human interaction._
>

Explainable models (XAI) are still in their infancy as of 2024[^1], but I believe they are essential to the future of artificial intelligence. Models right now are considered "black boxes"; their reasons for making a certain decision are completely unknown even to their programmers. If we want to put AI in important positions for medical diagnosis, law, and military usage, we want to be able to see why it is making the choices it makes.

Model interpretability is a loosely defined concept and does not
have a common quantitative measurement. Current explainability methods are all qualitative.
[You absolutely want to use this package for explaining your models](https://github.com/EthicalML/xai)
[YouTube Video on Types of Explainability](https://www.youtube.com/watch?v=Yg3q5x7yDeM)

There are a ton of types of machine learning models, and generally they decrease in explainability as they increase in complexity.

One big factor in explainability is also who you are explaining to. If you are creating XAI that is meant to be understood only by AI engineers, you can provide a lot of feedback that will be useful for improving the model. However, a consumer would not need this information. A banker who is using an AI model to determine whether or not someone is good for a loan will only require basic feedback.[^1]




[^1]: [Explainable Convolutional Neural Networks](https://dl.acm.org/doi/10.1145/3563691)