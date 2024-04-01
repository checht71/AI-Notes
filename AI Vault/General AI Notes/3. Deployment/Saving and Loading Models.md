
### PyTorch
In PyTorch, it's better to save a model dictionary rather than the entire model. This is supposed to make the model more flexible, more compatible with updates, and have it take less space. My guess is that PyTorch will build the model based on the instructions in the dictionary rather than load the whole thing in. Models in PyTorch are saved as `.pth` 

##### Saving the Model:
```python
# Save only the model state dict (recommended) 
torch.save(model.state_dict(), 'model.pth') 
# If you want to save the entire model 
torch.save(model, 'entire_model.pth')
```

##### Loading the Model for Deployment:
```python
# For loading the model state dict 
model = SampleModel() 
model.load_state_dict(torch.load('model.pth')) 
model.eval() # Put the model in evaluation mode 

# For loading the entire model 
entire_model = torch.load('entire_model.pth') 
entire_model.eval() # Put the model in evaluation mode
```


### TensorFlow
TensorFlow uses the `SavedModel` format. It used to use `h5`, but that's obsolete now. All you need to do to save a tf model is call `model.save()`