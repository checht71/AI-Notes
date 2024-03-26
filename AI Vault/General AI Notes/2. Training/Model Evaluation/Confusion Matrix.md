## Confusion Matrix
A confusion matrix is a way of visualizing the error of your network. The confusion matrix can also be used to derive most [[Model Evaluation|metrics]] such as accuracy, F1-score, precision, etc. easily. This can be done for the whole model or class based.

The x-axis represents the class that the model predicts during validation, and the y-axis represents the actual class of the object. This will give you an idea not only of how accurate the model is, but also how often it confuses one class with another specific class.
![[Pasted image 20230705154931.png|350]]
The above image is an example of a confusion matrix for a very small number of predictions. Road was predicted correctly twice, and one image of a road was mispredicted as a traffic sign. This tells you not only that the model is mispredicting, it tells you what it is mispredicting.

The sum of the diagonal of the confusion matrix is often used to evaluate the success rate of the neural network. This essentially yields the total correct predictions made.

Here's another image with more examples:
![[Pasted image 20230705155944.png|350]]