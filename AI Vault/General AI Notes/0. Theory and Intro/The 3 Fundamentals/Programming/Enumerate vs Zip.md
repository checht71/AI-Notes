Enumerate will return an index along with the value in the array. Zip will only return the values.


### Enumerate
```python
mylist = [3,2,1]
mylist_2 = [4,5,6]
for i,j in enumerate(mylist_2):
	print(i,j)
```
This returns:

| i | j |
| ---------- | --------- |
|0|4|
|1|5|
|2|6|

### Zip
```python
mylist = [1,2,3]
mylist_2 = [4,5,6]
for i,j in zip(mylist, mylist_2):
	print(i,j)
```


| i | j |
| ---------- | --------- |
|3|4|
|2|5|
|1|6|


>[!tip] TL;DR
>Enumerate will return an index of an array along with the array. Zip will pair two arrays together based on the positions of their elements.

