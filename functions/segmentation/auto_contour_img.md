# Automatic contouring based on the gray value image

The automatic contouring algorithm in the ORMIR_XCT package generates the periosteal mask of the distal and proximal bones of the wrist joint as well as a joint masking combining the distal and proximal bone masks. It uses the gray value image as input.

## Function
To use automatic contouring with a gray value image as input, use the following command:
```shell
autocontour(img, 
    mu_water, 
    rescale_slope, 
    rescale_intercept)
```

## Input parameter settings
````{tab-set}
```{tab-item} HR-pQCT
`img`: SITK image or path to image   
`mu_water`: Linear attenuation coefficient of water. Default = `0.2409`   
`rescale_slope`: Slope used to rescale to BMD. Default = `1603.51904`   
`rescale_intercept` Intercept used to rescale to BMD. Default = `-391.209015`   

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
Examples of how to use the function for the automatic contouring based on a gray value image as input can be found in:
* [Automatic contouring example](tutorials/Autormatic_Countour.ipynb) 
* [Bone mineral density analysis example](tutorials/Bone_Mineral_Density.ipynb)

Workflows that include automatic contouring: 
* [Automatic contouring workflow using the image as input](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/ormir_xct/workflows/autocontour_workflow.py)
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
> We used the method based on @10.1016/j.bone.2007.07.007 and implemented in ORMIR-XCT (@https://doi.org/10.21105/joss.06084).
```

```{tab-item} PCD-CT
Coming soon
```

```{tab-item} µCT
Coming soon
```
````
