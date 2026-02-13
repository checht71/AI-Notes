## [[Cross Entropy Loss]]
Cross entropy is the most simple type of loss function. 

## Mean Squared Error (MSE)
MSE is the most commonly used regression loss function. 

$$MSE = \frac{1}{n}\sum^n_{i=1}(\hat Y_i  -Y_i)^2$$
- $n$ = number of total training samples
- $i$ = a training sample (or batch)
- $Y$ = Actual value for the ith training sample
- $\hat Y$ = Predicted value for the ith training sample