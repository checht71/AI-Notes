[Video source](https://www.youtube.com/watch?v=Mrv3CZNWYEg)

## Strategies
#### REST API
Deploy the model on an API service such as [[FastAPI Overview|FastAPI]] or [[Flask Deployment|Flask]]. This is the most common way of deploying an AI model.
#### Edge Deployment
This is the deployment of an AI model on a small device such as a cell phone or a microcontroller. This can be done using methods like [[Quantization]] or using frameworks such as [[TensorFlow Lite]].
#### Batch Serving
Batch serving is manually collecting the data yourself, getting it onto the PC where you trained the model, and running the model on that data for your customer. This is the simplest and least powerful way of deploying a model.

## Basic Deployment
According to the video I watched, this is the most optimal basic method of deploying an AI.
![image](kub.png)
Create your model, create a flask/FastAPI application for it, wrap it in docker, and then use [kubernetes](https://www.youtube.com/watch?v=PziYflu8cB8) to manage how it is deployed.