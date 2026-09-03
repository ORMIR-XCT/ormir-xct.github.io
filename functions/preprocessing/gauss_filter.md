# Gaussian filtering

A Gaussian filter is an image-smoothing filter that reduces noise and small intensity variations by replacing each pixel or voxel with a weighted average of its neighbors, where closer neighbors receive higher weights according to a Gaussian (bell-shaped) distribution.

## Function
To use the Gaussian filter combined with a fixed threshold, use the following function:
```shell
seg_gauss(input_image,
    lower_threshold,
    upper_threshold,
    value_in_range,
    value_outside_range,
    sigma,
    support,
    use_image_spacing)
```

## Input settings
````{tab-set}
```{tab-item} HR-pQCT 

`input_image`: Gray value input image  
`lower_threshold`: Lower threshold for binarization  
`upper_threshold`: Upper threshold for binarization  
`value_in_range`: Value assigned to voxels inside the threshold range. Default = `127`  
`value_outside_range`: Value assigned to voxels inside the threshold range. Default = `0`  
`sigma`: Gaussian sigma. Default = `0.5`  
`support`:  Half-width of the Gaussian kernel in voxels. Default = `1.0`  
`use_image_spacing`: Whether sigma is interpreted in physical units. Default = `False`  

Further information about the function and its inputs can be found [here].
```

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

Examples of how to use the function for the Gaussian filtering can be found in: 
* [Trabecular segmentation example](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/examples/Trabecular_Segmentation.ipynb)
* [Laplace-Hamming filter example](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/examples/Laplace_Hamming_Filter.ipynb)

Workflows that include the Gaussian filter: 
* [Gaussian based segmentation](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/ormir_xct/workflows/seg_gauss_workflow.py)
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

If you use this function, please cite it like this:
> We used the method as implemented in ORMIR-XCT (@https://doi.org/10.21105/joss.06084).
```

```{tab-item} PCD-CT
Coming soon
```

```{tab-item} µCT
Coming soon
```
````
