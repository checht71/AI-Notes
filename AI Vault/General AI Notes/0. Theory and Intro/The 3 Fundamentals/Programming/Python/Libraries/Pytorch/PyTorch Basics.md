This is a quick overview of how to set up a neural network in PyTorch.

#### 1. Imports
In order to use PyTorch, you're gonna need multiple imports. Here's what they are and what they do:

```python
import torch
import torch.nn as nn
import torch.nn.functional as F
from torch.optim import SGD
```

`torch` includes the basics such as tensor objects and ways to manipulate them.
`torch.nn` includes specific neural network classes like dense, convolutional, and flattening layers.
`torch.nn.functional` contains activation functions such as ReLU and sigmoid.
`torch.optim` contains [[Optimizers]]. These include Adam and Stochastic Gradient Descent (SGD).

#### 2. The Neural Network Class
In order to create a neural network in PyTorch, you will have to specify the layers of the network and also the order which the data flows through the layers within a class that you define.

```python
# PyTorch models inherit from torch.nn.Module
class myNetwork(nn.Module):
    def __init__(self):
        super(SimpleClassifier, self).__init__()
        # define all the layers here and their parameters
        self.conv1 = nn.Conv2d(3, 6, 4)
        self.pool = nn.MaxPool2d(2, 2)
        self.conv2 = nn.Conv2d(6, 16, 5)
        self.fc1 = nn.Linear(13456, 120)
        self.fc2 = nn.Linear(120, 84)
        self.fc3 = nn.Linear(84, 4) # 4 is the num of classes

    def forward(self, x):
	    # specify how you want the data to flow through the layers here
        x = self.pool(F.relu(self.conv1(x))) # note that you can stack functions
        x = self.pool(F.relu(self.conv2(x)))
        x = x.flatten(x)
        x = F.relu(self.fc1(x)) # again, wrapping fc layer in activation func
        x = F.relu(self.fc2(x))
        x = self.fc3(x)
        return x
```