
## Resuming a Run
In order to resume a run, do the following:
When you pass `wandb.init()` include the argument `id=[run-id]` and then the id of the run that you're trying to resume. If that doesn't work, you can pass in `resume='must'` to try and force wandb to resume the run.
```python
wandb.init(id=[run-id], resume='must')
```
