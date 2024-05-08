KNN is a supervised learning classifier. It uses the distance between data-points in space to make classifications.

The training process for the KNN is incredibly simple: just create a plot of labeled data. That's literally it.

K is a hyperparameter that the user determines. If $k = 1$, the algorithm will only look at the nearest data-point and compare it to that. If $k = 6$, the algorithm will take the mode of the 6 nearest neighbors and sort the new point into that class.

![[Pasted image 20231113115851.png|550]]

### KNN for Image Classification
Using a KNN for image classification is a little bit more complicated than for simpler forms of data because we need to build our scatter plot from the feature space of the image.

#### Videos:
[KNN Theory](https://www.youtube.com/watch?v=HVXime0nQeI)
[Python Implementation](https://www.youtube.com/watch?v=rTEtEy5o3X0)
[KNN for Image Classification](https://www.youtube.com/watch?v=lGh_zCyY7TY)