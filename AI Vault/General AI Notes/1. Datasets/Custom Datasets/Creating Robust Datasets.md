## Why?
Machine learning is data driven. If you don't have high quality data, you can have some of the best ML models available, but your results would not be as good as if you had an average ML model trained on an excellent dataset.

- Simple models on large data sets generally beat fancy models on small data sets.

## What does a Good Dataset Look Like?
A good dataset has a good *Quantity* and *Quality of Images*

### Quantity
- As a rough rule of thumb, your model should train on at least an order of magnitude more examples than trainable parameters.
- Has a balanced number of images between each class

#### Quality
- Data is a good representation of what we want to predict on
- Are your features noisy
- Do your labels have mistakes in them?
- Minimal number of duplicates in dataset
- Normalize the data if possible using [[Batch Normalization]] or some other technique

## How to Get Data
1. Search for available datasets. They might help.
2. Manually collect and label data. Time consuming, expensive.
3. Use a  [[Generative Adversarial Network]] to create artificial data to train on.

## Data Pipelines
A #data-pipeline is a way to organize the flow of data.

Extract Transform Load (ETL) is a popular data pipeline in use. Here is the process:
- First, you determine what data you want to collect and from which sources.
- Next, you merge these data sources, transform the data to the required format, resolve inconsistencies, and fix errors.
- Afterward, you design data storage and store the processed and cleaned data there.
- Finally, you automate the entire process to run without human intervention. The data pipeline should be automatically triggered periodically or once a specific event occurs.




#### Links to Further Reading
https://developers.google.com/machine-learning/data-prep/construct/construct-intro
https://www.nature.com/articles/s42256-022-00516-1
https://www.youtube.com/watch?v=7XhDsbZyYoQ
https://datagen.tech/guides/image-datasets/image-datasets-for-machine-learning/
https://learn.microsoft.com/en-us/azure/cognitive-services/openai/how-to/prepare-dataset
https://pub.towardsai.net/how-to-create-a-new-custom-dataset-from-images-9b95977964ab
https://datagen.tech/guides/image-datasets/image-datasets-for-machine-learning/
https://cloud.google.com/vertex-ai/docs/tutorials/image-recognition-automl/dataset