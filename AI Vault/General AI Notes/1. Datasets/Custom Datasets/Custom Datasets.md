[Video](https://www.youtube.com/watch?v=NVxCKdp0NhQ)

This is the best method of data loading in PyTorch hands down.

This is the most basic format for a custom dataset in PyTorch:

```python
class myCustomDataset(Dataset): # must inherit from dataset class
def __init__(self):
	# load stuff in
	# split labels
	# convert to tensor
	# augment data
	# etc.

def __len__(self):
	return len(self.dataset)

def __getitem__(self, indx):
	return self.dataset[indx], self.labels[indx]
```

You NEED to build off of this format. You must inherit from `Dataset` and you must have `__init__` `__len__` and `__getitem__` as functions. You can add to this, but you cannot skip out on these.

### Using the Dataset
You can iterate over the dataset and index it as well, but what really makes a custom dataset useful is a dataloader!

```python
ds = myCustomDataset()

dataloader = Dataloader(ds, batch_size=64, num_workers=2, shuffle=True, drop_last=False)
```
Note:
	`num_workers` is the number of processes feeding data to the GPU. More workers = higher throughput = more resource intensive
	`drop_last` will drop extra data if it does not fit the batch size. For instance if you have 66 images and a batch size of 64, the last 2 images will be dropped.

Now you can iterate over your dataloader in a training loop!

### Training Loop

```python
for epoch in epochs:
	for data, label in dataloader:
		optimizer.zero_grad()
		output = model(data)
		loss_obj = F.nll_loss(output, label)

		loss_obj.backward()
		optimizer.step()

model.eval()
```


#### Things to Consider:
`__getitem__` must return tensors, numpy arrays, numbers, dicts or lists or else it will throw an error.