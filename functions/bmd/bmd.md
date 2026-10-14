# Bone Mineral Density

This function calculates the Bone Mineral Density (BMD) of an image in mgHA/ccm. 
If no mask is provided, BMD will be calculated for the entire image from its intensity. 
If a mask is provided, BMD will be calculated only for voxels inside the masked region.

## Function 

To calculate BMD, use the following commands:

```python
from ormir_xct.core.microarchitecture.bmd import bmd

bmd(
    image=value1,
    mask=value2,
    image_units=value3
    mu_scaling=value4,
    mu_water=value5,
    rescale_slope=value6,
    rescale_intercept=value7
    )
```

## Input settings

````{tab-set}
```{tab-item} HR-pQCT
`image`: Gray value image  
`mask`: Segmentation mask  
`image_units`: Input image units. Accepted values include `scanco`, `attenuation`, `hu`, `bmd`  
`mu_water`: Linear attenuation coefficient used for unit conversion. Default = `0.24090`  
`mu_scaling`: Scaling factor used for unit conversion. Default = `8192`  
`rescale_slope`: Calibration slope used for unit conversion. Default = `1603.51904`  
`rescale_intercept`: Calibration intercept used for unit conversion. Default = `-391.209015`

Further information about the function and its inputs can be found here (link to the API coming soon!)
```

```{tab-item} PCD-CT
Coming soon

```

```{tab-item} µCT
Coming soon

````
## Examples and workflows 

````{tab-set}
```{tab-item} HR-pQCT
Examples of how to use the BMD function:
- [Bone_Mineral_Density.ipynb](https://github.com/ORMIR-XCT/ormir-xct.github.io/blob/main/tutorials/Bone_Mineral_Density.ipynb)
```

```{tab-item} PCD-CT
Coming soon

```

```{tab-item} µCT
Coming soon

````

## Citation

````{tab-set}
```{tab-item} HR-pQCT
> We used the method implemented in ORMIR-XCT (@https://doi.org/10.21105/joss.06084).

```

```{tab-item} PCD-CT
Coming soon

```

```{tab-item} µCT
Coming soon

````