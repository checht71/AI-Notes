As machine learning projects develop, they become more automated. More automation leads to faster deployments, more reliability, and easier debugging.

There are 3 tiers of automation for machine learning:
1. **Manual Process:** Full experimentation pipeline executed manually using Rapid Application Development(RAD) tools, like Jupyter Notebooks. Deployments are also executed manually.
2. **Machine Learning automation:** Automation of the experimentation pipeline which includes data and model validation.
3. **CI/CD pipelines:** Automatically build, test and deploy of ML models and ML training pipeline components, providing a fast and reliable deployment.

There are a few tools for machine learning pipeline automation:

| Tool                      | License     | Notes                                                                                                                                                                                                                                                               |
| ------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DVC                       | Open-source | DVC can be used to make Data Pipelines, which can be automated and reproduced. Very useful if already using DVC for Data and Model versioning. Easily configured and run. Language and framework agnostic.                                                          |
| Tensorflow Extended (TFX) | Open-source | Used for production Machine Learning pipelines. Heavily integrated with Google and GCP. Only works with Tensorflow.                                                                                                                                                 |
| Kubeflow                  | Open-source | Kubeflow can build automated pipelines and experiments. Intended to build a complete end-to-end solution for Machine learning, being able to also serve and monitor models. Uses Kubernetes and is based on Tensorflow Extended. Works with Tensorflow and Pytorch. |
| MLflow                    | Open-source | Open-source platform for the machine learning lifecycle. Can be used with Python, Conda and Docker. Large community.                                                                                                                                                |
