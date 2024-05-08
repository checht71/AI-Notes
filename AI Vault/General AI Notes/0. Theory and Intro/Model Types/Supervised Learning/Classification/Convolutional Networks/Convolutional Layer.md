An image is based on the idea, that one pixel is dependent on its neighboring pixels, and the next pixel is dependent on its immediate neighboring pixels (be it color, brightness, contrast, and so on). CNN’s work on this idea, and uses filters on a patch of an image to extract important features and edges. This helps the model to learn only the necessary important features from an image, and not details of each pixel of an image.[{1}](https://towardsdatascience.com/are-transformers-better-than-cnns-at-image-recognition-ced60ccc7c8)


### Calculating Outputs of Conv2D Layers
Output Height = ((Input Height - Filter Height + 2 * Padding) / Stride) + 1 
Output Width = ((Input Width - Filter Width + 2 * Padding) / Stride) + 1