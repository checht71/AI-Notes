[Link](https://www.youtube.com/watch?v=NEaUSP4YerM)

## What is it?
t-SNE is a way of projecting data onto an axis while preserving the clustering of the original data. For example, if the data is separated into clusters on the y axis but we want to project it onto the x-axis, we lose information because the clusters will merge into one another. With t-SNE, the clusters are offset when projected onto the x-axis.

TL;DR: t-SNE is a way of preserving multi-dimensional data during compression/projection into a lower dimensional space.

## ML Applications
t-SNE is a visualization technique. Neural networks work with tensors which can be tens to hundreds of dimensions, and t-SNE is a way of projecting that data into 2D or 3D so that humans can comprehend it without losing too much of the characteristics of the original higher dimensional data. One big use of t-SNE in particular is to visualize the network activation in a layer.

"Tight clusters in the resulting t-SNE plot correspond to classes that the network usually classifies correctly. The visualization thus made it possible to evaluate readily which observation that the network misclassified." [[Evaluation of deep learning models for classification of asphalt pavement distresses|Source]] 