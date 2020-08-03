# Contributing

We welcome contributions to the MachineLearningNotebooks.

## Style Guidelines 

### Variable names 

```python
from azureml.core import Workspace

# get workspace 
ws = Workspace.from_config()

# access assets 
dstore = ws.datastores['my-datastore']
dset = ws.datasets['my-dataset']
env = ws.environments['my-environment']
model = ws.models['my-model']
ct = ws.compute_targets['my-compute']
```