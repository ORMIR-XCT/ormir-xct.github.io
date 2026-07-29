# Local adaptive thresholding


## Theoretical background 
Local adaptive thresholding compute a threshold for each voxel using the intensity range of neighboring voxels. It contrast with the fixed global threshold that uses a single threshold for the entire image. 
 
To use local adaptive thresholding with the default input settings, use the following command:
```shell
adaptive-local-threshold
```

## Input parameter settings
````{tab-set}
```{tab-item} HR-pQCT
The following input settings are used for the local adaptive thresholding:
```shell
lower_threshold: float = 190
upper_threshold: float = 450
structuring_element_size: int = 6,
```
````

## Examples and workflows
Workflows that include local adaptive thresholding: [local adaptive thresholding](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/ormir_xct/workflows/adaptive_local_threshold_workflow.py).


If you use this filter, please cite @https://doi.org/10.1093/jbmrpl/ziag054.