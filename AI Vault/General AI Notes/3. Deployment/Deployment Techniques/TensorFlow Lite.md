[Tutorial Link](https://www.youtube.com/watch?v=OJnaBhCixng)
[Google Colab Link](https://colab.research.google.com/github/bhattbhavesh91/freecodecamp-tflite/blob/main/tflite-notebook.ipynb)

Edge Devices - Small devices such as phones, wearables and microcontrollers that can run simple neural networks
Edge Computing - moving computing into these edge devices

One alternative to edge computing is cloud computing, where the neural network is housed on a server and queried.

##### Why Edge Computing?
- Much Lower Latency
- No internet needed
- Much more User Privacy

##### Cons of Edge Computing:
- Limited computation power
- Limited memory
- Battery consumption
- Increased app size vs cloud computing

#### You convert a tensorflow model to TF Lite similar to TF JS. 
1. create model
2. covert (done in IDE)
3. deploy on edge device

### Convertsion Code
````
# Converting a SavedModel to a TensorFlow Lite model.  
converter = tf.lite.TFLiteConverter.from_saved_model(saved_model_dir)  tflite_model = converter.convert()
# Converting a tf.Keras model to a TensorFlow Lite model.converter = tf.lite.TFLiteConverter.from_keras_model(model)
tflite_model = converter.convert()
````

The model you get wil be about 1/3 the size of the original.

## Model Validation
You should validate a model after converting it, because its essentially a different model based off of your original.


### Run a TF Lite file in Python

```
tf.lite.Interpreter(model_path=model_path)
```


Make sure the input and output tensors are the same as your original model, because they can change during the conversion process.


## Further Compression
Models can be compressed by reducing the weights, inputs, and outputs from 32 bit to 16 bit. This will reduce the amount of information that the network processes and maybe also reduce the accuracy depending on the network (more accurate networks would suffer more from this).



Models can also be supercompressed using a process called #Quantization. Quantization is compressing the amount of space that activation functions and weights take up. How does it do this?
Each weight in your network has a specific value, which is usually a long float such as 3.1234561. Quantization basically takes this and all of the other weights in your network and rounds them to the nearest whole number. So in this case, the weight for the new network will be 3. This may compromise on the accuracy of your network a little bit or it may do nothing, so it is important to validate the network after Quantization.