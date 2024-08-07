[main video source](https://www.youtube.com/watch?v=Mrv3CZNWYEg)

Any type of model deployment is known as *model serving*. Model serving is taking a model that you have trained and setting it up so that it can take new inputs from users and return outputs such as predictions.[^1]
## Strategies
#### A. REST API
Deploy the model on the web and let users send and receive information. This is done using a [[Choose a Serving Framework|serving framework]]. This is the most common way of deploying an AI model.
#### B. Edge Deployment
This is the deployment of an AI model on a small device such as a cell phone or a microcontroller. This can be done using methods like [[Quantization]] or using frameworks such as [[TensorFlow Lite]].
#### C. Batch Serving
Batch serving is manually collecting the data yourself, getting it onto the PC where you trained the model, and running the model on that data for your customer. This is the simplest and least powerful way of deploying a model.

## Basic REST Deployment
According to the video I watched, this is the most optimal basic method of deploying an AI.
![image](kub.png)
Create your model, create a flask/FastAPI application for it, wrap it in docker, and then use [kubernetes](https://www.youtube.com/watch?v=PziYflu8cB8) to manage how it is deployed.


# Strategy A. REST API
## Stage 1: Train & Save the Model
You should know how to do this by now if you're trying to deploy it.
## Stage 2: Create a Web App and Dockerize it
This can be done using any of the REST APIs, but your best bet is to use [[BentoML Dev Process]] since it is optimized for running machine learning models, but you can also use [[FastAPI Overview|FastAPI]] or [[Flask Deployment|Flask]].
## Stage 3: Deploy at Scale
Use a hosting service to take your web app and handle the incoming and outgoing data. These services will also scale the amount of instances open at a single time based on the amount of traffic.

# Strategy B. Edge Deployment
idk lol but you should definitely [[Quantization|Quantize]] your model so that it can run fast on edge devices and use a framework such as [[TensorFlow Lite]].


![[Pasted image 20240726151547.png]]
[^2]

[^1]: [How to Serve PyTorch Models with TorchServe](https://www.youtube.com/watch?v=XlO7iQMV3Ik)
[^2]:https://ml-ops.org/content/end-to-end-ml-workflow