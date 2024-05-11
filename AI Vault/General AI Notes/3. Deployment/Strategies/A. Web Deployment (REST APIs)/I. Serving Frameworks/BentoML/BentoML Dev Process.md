All of the information below is from this [Video](https://www.youtube.com/watch?v=HHkmfI_yncc)

BentoML is a python package that you can install with pip just like any other.
```bash
pip install bentoml
```

Here's the steps on how to deploy a model using BentoML:
1. Train your model
2. Save the model to BentoML local store
3. Create a BentoML Service
4. Create a *bento*
5. Serve the model through a *bento*
6. Dockerize the *bento*
7. Run the bento service via Docker.

### 2. Save the model to BentoML local store
Doing this is an easy one liner that is very similar to the way you would normally save and load a model. In addition to `bentoml.keras`, there's also `bentoml.scikit` and `bentoml.torch`.
```python
import bentoml

bento_model = bentoml.keras.save_model(<name>, model)
print(bento_model.tag)
```

You can check what's saved in the local store by typing `bentoml models list`. The bento model tag is needed to create a service from your model.

### 3. Create a BentoML Service
A BentoML service is an equivalent to [[Flask Deployment|Flask]] or [[FastAPI Overview|FastAPI]]. It creates a webapp from your code and allows you to build endpoints to expose to the world. You can also convert your model into a `runner`, which automatically optimizes your model for deployment and gives you additional functionality.

```python
import numpy as np
import bentoml
from bentoml.io import NumpyNdarray

BENTO_MODEL_TAG = "keras_model:xnrcktalj2nplcoq"

#convert model to runner
classifier_runner = bentoml.keras.get(BENTO_MODEL_TAG).to_runner()

mnist_service = bentoml.Service("mnist_classifier", runners=[classifier_runner])

#create the get request and set the input and output types
@mnist_service.api(input=NumpyNdarray(), output=NumpyNdarray())
def classify(input_data: np.ndarray) -> np.ndarray:
    return classifier_runner.predict.run(input_data)
```

At this point, you can technically send a [request to this service](https://youtu.be/HHkmfI_yncc?si=SQIjKHczUHXQtcdp&t=928), but we're going to take it further in order to make things even better.
### 4. Create a *bento*
To create a bento file, we have to make a file named `bentofile.yaml`. This file contains information about the service, metadata, files, and the packages needed to make the program run.
```yaml
service: "service:mnist_service"  # Same as the argument passed to bentoml
labels:
  owner: Valerio
  stage: dev
include:
  - "*.py"  # A pattern for matching which files to include in the bento
python:
   packages:  # Additional pip packages required by the service
     - tensorflow
     - numpy
```

once you have created your file, open the terminal in its directory and type in `bentoml build`.

### 5. Serve the model through a *bento*
Use `bentoml serve <bento tag> --production` in the terminal to serve the model. You can check the tags using `bentoml list`. 

### 6. Dockerize the *bento*
Run `bentoml containerize <bento tag>` to create a Docker image from your bento. This will get your bento ready for Docker. This will take some time.

### 7. Run the bento service via Docker
In the terminal write `docker run -p 3000:3000 <bento tag>`. 
	This will run docker and map port `3000` inside the container to port `3000` outside the container, essentially just making sure your endpoint has a clear path in and out.

## Next Stages
Now that you have the docker image of your bento done, it is ready to deploy at scale.

### Deployment Options
- Kubernetes -> Yatai
- Any cloud platform -> bentoctl