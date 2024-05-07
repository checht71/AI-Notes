## BentoML
BentoML is probably your best bet for deploying AI models. It is similar to FastAPI and Flask, but the key difference is that those 2 are for general purpose apps. BentoML is specifically for designing and deploying machine learning models. It will optimize your model for you so that your webapp runs much quicker than if you were to use the alternatives. Also open source. Packages all necessary artifices (model+code) in an object called a *Bento*. Supports all major ML libraries. Integrates with Docker. You can also deploy on Kubernetes with an extension called [Yatai](https://github.com/bentoml/Yatai). Automatically generated documentation. Works only with Python. Deployment only.
## TensorFlow Serving
Deployment framework within the TensorFlow sphere. Only good for TensorFlow models of course. Documentation is not great for this.
## TorchServe
The [[PyTorch Basics|PyTorch]] version of TensorFlow serving.
## ML Flow
A framework that takes care of the entire life cycle of a machine learning project. ML Flow model is a standard that allows you to package an AI model for production. You can 'dockerize' your AI model easily with this. It can only be easily deployed into SageMaker and [[Azure Guide|Azure]].
## Seldon
Another framework that takes care of the entire life cycle of a model. It is the best and easiest out of the 3, but it is not free or open source.
## KServe
Free and open source part of kubflow, an ML workflow framework. Free and open source, used by google. Allows direct serving to a kubernetis cluster. Complex to set up. You can only use Kubernetis to deploy if you use this option.



##### [Video Source](https://www.youtube.com/watch?v=Mrv3CZNWYEg)