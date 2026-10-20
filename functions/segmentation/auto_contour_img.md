# Automatic contouring

The automatic contouring algorithm generates the periosteal mask of the bone based on the gray value image.

## Function
To use automatic contouring, use the following commands:

```python
from ormir_xct.core.segmentation.autocontour import autocontour

autocontour(img, 
    mu_water, 
    rescale_slope, 
    rescale_intercept)
```

## Input settings
````{tab-set}
```{tab-item} HR-pQCT
`img`: SITK image or path to image   
`mu_water`: Linear attenuation coefficient of water. Default = `0.2409`   
`rescale_slope`: Slope used to rescale to BMD. Default = `1603.51904`   
`rescale_intercept` Intercept used to rescale to BMD. Default = `-391.209015`   

Further information about the function and its inputs can be found here (link to the API coming soon!)
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
Examples of how to use the function for the automatic contouring can be found in:
* [Automatic contouring example](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/examples/Automatic_Contour.ipynb) 
* [Bone mineral density analysis example](https://github.com/ORMIR-XCT/ormir-xct.github.io/blob/main/tutorials/Bone_Mineral_Density.ipynb)

Workflows that include automatic contouring: 
* [Automatic contouring workflow](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/ormir_xct/workflows/autocontour_workflow.py)
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
> We used the method by @10.1016/j.bone.2007.07.007 and implemented in ORMIR-XCT (@https://doi.org/10.21105/joss.06084).
```

```{tab-item} PCD-CT
Coming soon
```

```{tab-item} µCT
Coming soon
```
````
