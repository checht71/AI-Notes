#overfitting 

### Overview
Overfitting is something that happens when a model begins to recognize and predict based on noise within data. This generally happens in small datasets where there is not a lot of variance in the data or there are extraneous similarities between classes.
Overfitting can be a serious problem because it will give false accuracy in your training/validation results. You can check if your model is overfit in a few ways:
1. Run the model on a test dataset. (This will not be reliable if your test dataset has the same flaws as your training dataset.)
2. Print/export the values of the weights. If some of the weights are very high, that is a sign that the model is overfit.

The reason behind why the model may be overfit if the weights are too high is that a high weight assigns a high amount of importance of a specific input to a specific output. This "Overspecificity" is what causes overfitting.


### What can be done about overfitting?
1. [[Regularization]]
2. [[Data Augmentation]]
3. [[Creating Robust Datasets]]
4. [[Transfer Learning]]
5. [[Cross Validation Sampling]]
6. [[Feature Reduction]]
7. [[Batch Normalization]]