PyTorch is a more in depth class based version of tensorflow.

PyTorch is a lot more similar to the mathematics. You define a lot more of the parameters manually.

Your model is defined within a class:
```python
class ImageClassifier(nn.Module):
	def __init__(self): #Create model here
	super().__init__() #boilerplate
	self.model = nn.Sequential(
	nn.Conv2d(1, 32, (3,3)), #1 channel, 32 filters, 3x3 kernel
	nn.ReLU(),
	nn.Conv2d(32, 64, (3,3)),
	nn.ReLU(),
	nn.Conv2d(64, 64, (3,3)),
	nn.ReLU(),
	nn.Flatten(),
	nn.Linear(64*(28-6)*(28-6), 10),
	)

def forward(self, x):
	return self.model(x)
```

## Device Selection
In PyTorch, you manually select whether to use the CPU or GPU. The way you do this is by setting the parameter `device` equal to `cpu` or `gpu`.
