# Contributing

We welcome contributions to the MachineLearningNotebooks.

## Style Guidelines 

### License Cell

The first cell should be markdown and contain the copyright and license:
```
Copyright (c) Microsoft Corporation. All rights reserved.

Licensed under the MIT License.
```

### Get Workspace

The second cell should get and print the Azure ML Workspace.

```python
from azureml.core import Workspace

# get workspace 
ws = Workspace.from_config()
ws
```

### Common assets 

Common ML assets can be obtained from the Workspace object. 

```python
# get assets 
ct = ws.compute_targets['my-compute']
env = ws.environments['my-environment']
dset = ws.datasets['my-dataset']
model = ws.models['my-model']
dstore = ws.datastores['my-datastore']
```

### Compute Targets 

Compute targets are preconfigured in the [setup.ipynb](setup.ipynb) notebook named `cpu-cluster` and `gpu-cluster`. Use these compute targets in notebooks. 

## Conventions

### Remote runs

Estimators should not be used. Instead, a `ScriptRunConfig` should be used with a curated Azure ML Environment. Datasets should be used.  