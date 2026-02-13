A centroid is the point in a system of masses each of whose coordinates is a weighted mean of coordinates of the same dimension of points within the system, the weights being determined by the density function of the system.

$$ Centroid (X, Y) = \frac{w_1(x_1,y_1) + ... + w_n(x_n,y_n)}{n}$$
	Where:
	($x$,$y$) is a tuple of coordinates (a coordinate pair),
	$n$ is the number of points in the shape,
	$w_n$ is the weight at point $(x_n,y_n)$ derived from the density function of the shape.

![[Pasted image 20231102141429.png|500]]
## Uses in the WokMatic
The centroid is used in the WokMatic for a few of our position distance loss functions. The biggest example is the [[Solutions Document Loss Functions|Pointwise Euclidean Distance]]. Since there is no density function for the points in this problem, we can interpret the centroid as _the average of coordinates_.

$$ Centroid (X, Y) = \frac{(x_1,y_1) + ... + (x_n,y_n)}{n}$$
	Where $n$ is the number of points in the shape.
