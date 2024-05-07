Quantization is a machine learning technique that is applied after training in order to maximize the speed of the model during deployment at the cost of some accuracy. Quantization is really just a fancy way of saying compression.

![[Quantization.png]]

The most common way of performing quantization of a model is to change the data types of the model parameters. For example, by default the weights of a model are float32 (32 bit float). To save space, they can be converted to float16 or even int8. This will reduce the amount of bits that each weight takes up, reducing the calculations your model has to do to predict.