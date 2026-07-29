# Joint space parameter calculation

Joint space parameter calculation uses the joint space mask to calculate joint space volume, mean width, width standard deviation, minimum width, maximum width, asymmetry, and bone-on-bone contact.

## Function

To calculate the joint space parameters, use the following function:

```shell
jsw_parameters(
    pad_image,
    dilated_js_mask,
    filename,
    output_path,
    js_mask,
    voxel_size,
    oversamp,
    skel,
    minimum)
```

## Input settings

````{tab-set}
```{tab-item} HR-pQCT 

`pad_image`: Padded binary image of the joint segmentation  
`dilated_js_mask`: Dilated binary joint space mask  
`filename`: Name used for the output file  
`output_path`: Directory where the output file will be saved  
`js_mask`: Binary joint space mask  
`voxel_size`: Image voxel size. Default = `0.0607`  
`oversamp`: Enables oversampling during the width calculation. Default = `True`  
`skel`: Enables skeletonization during the width calculation. Default = `True`  
`minimum`: Minimum width value included in the calculation. Default = `0.0`  

Further information about the function and its inputs can be found [here (tbd)]().
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

Examples of how to use joint space parameter calculations:
- [Finger_Joint_Comparison.ipynb](https://github.com/ORMIR-XCT/ormir-xct.github.io/blob/main/tutorials/Finger_Joint_Comparison.ipynb)

Workflows that include joint space parameter calculations:
- [JSW analysis workflow](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/ormir_xct/workflows/jsw_analysis_workflow.py)
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
> We used the method from @10.1046/j.1365-2818.1997.1340694.x as implemented in ORMIR-XCT (@https://doi.org/10.21105/joss.06084).

```

```{tab-item} PCD-CT

Coming soon
```

```{tab-item} µCT

Coming soon
```
````
