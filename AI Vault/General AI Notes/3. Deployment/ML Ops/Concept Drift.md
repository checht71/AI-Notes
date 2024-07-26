Concept drift is when you deploy a machine learning model and you find out that the data that is actually being collected differs from the data you used to train the model, throwing off the results. 

For instance, if you take a bunch of images during the daytime when there are no shadows for your training set and after deployment users send images during sunset when there are shadows.

### Two Types of Concept Drift

In order to better understand the effects of concept drift, we need to distinguish between two types of concept drift:

- **Virtual drift** – when p(X) changes but p(Y|X)does not change. Meaning that there was a change in the features’ underlying distribution, but the model’s performance hasn’t changed.
- **Real drift** – there was a change in p(Y|X), meaning the performance of the model changed.[^1]


[^1]: https://ai-infrastructure.org/concept-drift-in-machine-learning-101/