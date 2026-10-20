# Adaptive local thresholding

Local adaptive thresholding computes a threshold for each voxel using the intensity range of neighboring voxels. 
This contrast with fixed global thresholding — adopted in the Gaussian and LaplaceHamming filter — which  uses a single threshold value for the entire image.

## Function
To use local adaptive thresholding with the default input settings, use the following commands:

```python
from ormir_xct.core.segmentation.adaptive_local_threshold import adaptive_local_thresholding

adaptive-local-threshold(
    structuring_element_shape,
    structuring_element_size,
    lower_threshold,
    upper_threshold,
    local_threshold_method,
    sigma,
    minimum_structure_size,)
```

## Input settings
````{tab-set}
```{tab-item} HR-pQCT

`image_sitk` : Image to threshold, accepts string paths  
`structuring_element_shape`: Shape of the structuring element, accepts `ball` or `cube`. Default = `ball`   
`structuring_element_size`: Size of structuring element. Default = `6`
`lower_threshold`: The lower threshold. Default = `190`  
`upper_threshold`: The upper threshold. Default = `450`  
`local_threshold_method`: The method to use for identifying local thresholds. Accepts `mean`, `minmax`, or `both`. Default = `mean`   
`sigma`: The sigma to use for the gaussian filter. Default = `None`  
`minimum_structure_size`: The minimum size of structures to keep in the segmentation. Default = `64`  
```
Further information about the function and its inputs can be found here (link to the API coming soon!)

```{tab-item} PCD-CT
Coming soon
```

```{tab-item} µCT
Coming soon
```
````

## Examples and workflows
````{tab-set}
```{tab-item} HR-pQCT 

Workflows that include the local adaptive thresholding:  
* [Adaptive local thresholding](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/ormir_xct/workflows/adaptive_local_threshold_workflow.py).
```

```{tab-item} PCD-CT
Coming soon
```

```{tab-item} µCT
Coming soon
```
````

## Citation
````{tab-set}
```{tab-item} HR-pQCT 

If you use this function, please cite it as follows:
> We used the adaptive local thresholding as implemented in ORMIR-XCT (@https://doi.org/10.21105/joss.06084).
```

```{tab-item} PCD-CT
Coming soon
```

```{tab-item} µCT
Coming soon
```
````
