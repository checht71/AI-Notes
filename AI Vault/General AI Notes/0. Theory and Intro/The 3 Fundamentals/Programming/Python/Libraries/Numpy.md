A foundational package for numerical computing in python. Primarily used for manipulation of arrays and matrices.


### Helpful Numpy Tips:

##### [np.empty](https://numpy.org/doc/stable/reference/generated/numpy.empty.html)
Creates an empty array of a size you specify.

##### np.concatenate vs append:
It's better to concatenate arrays using numpy rather than using the append function. This is more efficient because append creates new copies of an array every single time it is called, therefore making it more inefficient when used in a loop.

###### append vs extend:
append will add a single element onto a numpy array or default list. Extend will concatenate two default lists together.
