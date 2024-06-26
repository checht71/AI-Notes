#### Confusion Matrix
A [[Confusion Matrix]] is a good way to visualize most of these metrics, and it can also help you derive them in some cases.

## Accuracy:
Accuracy is the simplest method of model evaluation. Out of the total amount of images, how many were correctly predicted? This metric can give you a decent feel for a model, but sometimes it is too simple to get a good picture of what's going on with the model.

$$Accuracy = \frac{Correctly\;Predicted\;Samples}{Total\;Samples}$$

## Top-N Accuracy:
This is a less rigid form of accuracy that kind of feels like cheating. Take a number $n$. Usually $n$ is 1 or 5. If $n=5$, than if the actual label is in the top 5 predictions that the network makes before argmax, then it is counted as "correct". 

## Precision:
Precision is a step up from accuracy. Precision looks at all of the positive predictions that a model makes and sees how many of them were correct.

$$Precision = \frac{Correct\;Positive\;Predictions}{Total\;Positive\;Predictions}$$

## Recall:
Recall goes hand in hand with precision. Recall looks at all of the _actual_ positives vs. the positives which the AI picked up.

$$Recall = \frac{Correct\;Positive\;Predictions}{Total\;Positive\;Samples}$$

![400](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2Fthumb%2F2%2F26%2FPrecisionrecall.svg%2F700px-Precisionrecall.svg.png&f=1&nofb=1&ipt=f450866a03cc49cf82a9826ae17b6dc81421070e5b4730af7cd3480d5f91c76b&ipo=images)

## F1 Score:
The F1 score is a way of combining precision and recall into a single metric. It is best used with other metrics.

$$F1 = \frac{2}{(1/Precision)+(1/Recall)}$$

### Example:
Let's say in a cats dogs dataset had 20 images and the AI predicted 10 cats and 10 dogs. The actual dataset had 12 dogs and 8 cats.  9 of the images that were dogs were correctly predicted, 1 image was a cat. 7 of the images that were cats were correctly predicted, 3 of them were dogs. Let's find the precision and the recall for these predictions.

$$Accuracy = \frac{Correctly\;Predicted\;Samples}{Total\;Samples} = \frac{16}{20} = 0.8$$
$$Precision = \frac{Correct\;Positive\;Predictions}{Total\;Positive\;Predictions}= \frac{9}{10} = 0.9$$
$$Recall = \frac{Correct\;Positive\;Predictions}{Total\;Positive\;Samples} = \frac{9}{12} = 0.75$$
$$F1 = \frac{2}{(1/Precision)+(1/Recall)} = \frac{2}{(1/0.9)+(1/0.75)}=0.81$$

Note: Keep in mind that precision and recall only work on one class at a time. One way to get around this is to take the precision and recall for every class and then average them all out together.

## Precision-Recall (PR) Curve
A comparison of what the recall is when precision is at a certain value and vice versa on a graph.

![350](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fuser-images.githubusercontent.com%2F26833433%2F76019078-0a79fb00-5ed6-11ea-8b5b-5697bbbd7e7e.png&f=1&nofb=1&ipt=7b17f02d7cd87ef839e58c4c8ecaf27b77f3726628b9c5c981952a2ae726c84c&ipo=images)

### Mean Average Precision (mAP)
mAP is the area under the P-R Curve. This metric is used mainly in object detection models such as YOLO and Faster-RCNN.
## ROC Curve (AUC)
Compares the true positive rate with the false positive rate on a graph.
![[Pasted image 20230705163331.png|400]]
The area under the curve for both of these types of graphs is usually taken. Sometimes this is shortened to AUC. You want the AUC to be at a maximum value (1) to ensure that your model is performing the best. AUC is considered a more robust measure of performance than some of previously reviewed measures such as accuracy, F1-score and recall as it is not affected by class imbalance.

## Crossentropy:
Crossentropy is a way of comparing the output of the model with the actual data. For example: if my output is supposed to be $[ 0, 1, 0 ]$ and the model predicts $[0.05, 0.85, 0.10]$, the crossentropy is .15 because that's how incorrect the model's prediction was.

## Mean Absolute Error (MAE)
Mean absolute error is taking the absolute values of all of the errors and the finding their mean.

## Mean Squared Error (MSE)
This is a version of mean absolute error that focuses a little bit more on the greatest error values.

## Root Mean Squared Error (RMSE)
Pretty much what it sounds like. Taking the root of the mean squared error so that it's easier to interpret and looks prettier.

## R2 (Coefficient of Determination)
R^2 is a way of seeing how well a curve fits data. The farther away the data is from the curve, the lower R2 will get. If the data perfectly fits the line R2 = 1. 

## Cosine Similarity
Similar to crossentropy but for regression problems. Tells us how similar 2 different vectors are to each other.

## Matthews Correlation Coefficient (MCC)

$$ 

MCC = \frac{t_p*t_n-f_p*f_n}{\sqrt{(t_p+f_p)*(t_p+f_n)*(t_n+f_p)*(t_n+f_n)}}

$$
Where $t_p$ = True positive
$t_n$ = True negative
$f_p$ = False positive
$f_n$ = False negative

MCC represents a correlation coefficient between the measured and predicted classifications and has values that range from −1 to +1, where a value of +1 represents a perfect prediction, 0 is no better than random prediction, and −1 represents the worst possible prediction.

This is considered to be a more reliable result, as the MCC is only +1 if all four categories of the [[Confusion Matrix]] are the correct values.

## Ambiguity Parameter
This is a metric used particularity in CNNs. Sometimes classes can be very similar to one another, and it can be very difficult to discern differences between them. In other words, they are *ambiguous*. The ambiguity parameter is the ratio between the first ranked prediction and the second ranked one. This ranges from 0 to 1. 0 means the network is certain in its decision making, 1 means that the network is confused. Keep in mind, the network being sure about its decisions does not necessarily mean that it is accurate in those decisions.

##### More Info
Visit the libraries of Scikitlearn, Keras or Tensorflow, you will find even more ways of assessing AI.

# Logging
In order to actually track and monitor these metrics, you have to use a #logger. A logger is basically just a way of tracking these metrics. There are a few different ones you can use.
[[Weights and Biases Logging]]: this is one of the most powerful. If you have an online account, it will save data from every run to your profile (up to 100 GB worth) for you to view at any time.
- [[Tensorboard]]: this is Tensorflow's built in logger.
- Console Logging: The one you're probably most familiar with. It just outputs the metrics into the console.
- Text Logging: The same thing as console logging, but just exported to a text file.

[Source](https://www.youtube.com/watch?v=LbX4X71-TFI)