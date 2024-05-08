$$
IOU = \frac{A \bigcap B}{A\bigcup B}
$$
This is the same as saying "A AND B DIVIDED BY A OR B". Another way of looking at this is saying that the intersecting area is divided by to the total area of A and B.

This is a normalized measure of overlap from 0 to 1.

 

#### Machine Learning Use Cases
This function has further use in machine learning as a whole, particularly object detection.
Imagine you create a bounding box around a cat as a label (green in below figure). Then you have the AI model predict where the cat is (the blue label below). The aim of this model would be to keep improving its prediction, until the blue box and the green box perfectly overlap, i.e the IOU between the two boxes becomes equal to 1.

![IOU Image](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.FV4Wj_kj2e1zEBm_fWzojQHaF7%26pid%3DApi&f=1&ipt=0c35890307133c44ae0c1ade82c281d62772c8385037a04257985fc3b9d9197f&ipo=images)

Another use case for IOU is for the [[Solutions Document Loss Functions|WokMatic Problem]] that I worked on. We tried to make an AI generated set of coordinates map to a set of human coordinates. To do this, one of the equations recommended was the IOU.

### Issues with the IOU
The IOU will give you plenty of information regarding _how much_ of an area is overlapping with another, but not _how_ it's overlapping or what direction it needs to go to achieve that. If the two sections are [[Disjoint|disjoint]], there's no way they IOU will provide you with the direction that the prediction box needs to go to align with the detection box. Whether this works out when the AI just randomly predicts a box that overlaps is yet to be seen by me. How much it slows down the training process I have also yet to see.

[Article](https://medium.com/analytics-vidhya/iou-intersection-over-union-705a39e7acef)

