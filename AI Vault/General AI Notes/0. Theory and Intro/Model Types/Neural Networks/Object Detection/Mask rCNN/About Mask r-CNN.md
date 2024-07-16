- [Mask r-CNN Github](https://github.com/matterport/Mask_RCNN)
- [Everything about Mask R-CNN: A Beginner’s Guide](https://viso.ai/deep-learning/mask-r-cnn/)
- [Mask RCNN Quick Explanation](https://medium.com/@tibastar/mask-r-cnn-d69aa596761f)
- [Installing Mask RCNN](https://www.youtube.com/watch?v=GSDbfGsxruA)
- [Object detection using Mask R-CNN on a custom dataset](https://towardsdatascience.com/object-detection-using-mask-r-cnn-on-a-custom-dataset-4f79ab692f6d)
- [Official MaskRCNN Article](https://engineering.matterport.com/splash-of-color-instance-segmentation-with-mask-r-cnn-and-tensorflow-7c761e238b46)

## About Mask RCNN
RCNN - Regional Convolutional Neural Network

Mask RCNNs can input images or video and output bounding boxes, masks, and classes. You can take the area of the masks as well, which makes it extremely helpful for finding the area of the deformations.
Mask RCNN uses instance segmentation -  a form of image segmentation which sees individual objects at the pixel level rather than just classes. For example - it will see 3 seperate cars in an image rather than just saying "this image contains a lot of car in it", which is how semantic segmentation works.

RCNNs first find possible bounding boxes within an image, then sends them deeper into the network so that masks can be fit to them at a pixel scale and they can be classified.

Faster RCNN is better because uses a "Region Proposal Network". It does a much quicker job at assigning the intial possible bounding boxes for the input. An RCNN submits over 2000 possible bounding boxes, while the faster RCNN does it in one sweep.
