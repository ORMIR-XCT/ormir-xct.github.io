# Bone Mineral Density

The Bone Mineral Density (BMD) function calculates the BMD of an image in mgHA/ccm. If no mask is provided, BMD will be calculated for the entire image from the intensity information provided by the image. If a mask is provided, BMD will be calculated only for voxels inside the mask region.

## Function 

Use this command:

```shell
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

For further information about the function and inputs, visit [here (tbd)]().

```

```{tab-item} PCD-CT
**Coming Soon**

```

```{tab-item} µCT
**Coming Soon**

````
## Examples and workflows 

````{tab-set}
```{tab-item} HR-pQCT
Examples of how to use the BMD function:
- [Bone_Mineral_Density.ipynb](https://github.com/ORMIR-XCT/ormir-xct.github.io/blob/main/tutorials/Bone_Mineral_Density.ipynb)
- [Bone Mineral Density Example](https://ormir-xct.github.io/tutorials/bone-mineral-density/)

```

```{tab-item} PCD-CT
**Coming Soon**

```

```{tab-item} µCT
**Coming Soon**

````

## Citation

````{tab-set}
```{tab-item} HR-pQCT
> We used the method implemented in [](https://doi.org/10.21105/joss.06084)

```

```{tab-item} PCD-CT
**Coming Soon**

```

```{tab-item} µCT
**Coming Soon**

````