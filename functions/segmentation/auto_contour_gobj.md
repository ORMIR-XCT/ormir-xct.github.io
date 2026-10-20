# Automatic contouring based on a rough existing periosteal mask

This variation of [automatic contouring](./auto_contour_img.md) uses the gray value image as well as a rough periosteal mask of the bones as input and generates a refined periosteal mask.

## Function
To use automatic contouring based on an existing periosteal mask, use the following commands:

```python
from ormir_xct.core.segmentation.autocontour import autocontour_gobj

autocontour_gobj(
    img, 
    dst_gobj, 
    prx_gobj):
```

## Input settings
````{tab-set}
```{tab-item} HR-pQCT
`img`: SITK image or path to image   
`dst_gobj`: SITK image or path to distal periosteal mask
`prx_gobj`: SITK image or path to proximal periosteal mask

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
Examples of how to use the function for the automatic contouring based on an existing periosteal mask can be found in:
* [Automatic contouring example](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/examples/Automatic_Contour.ipynb) 
* [Bone mineral density analysis example](https://github.com/ORMIR-XCT/ormir-xct.github.io/blob/main/tutorials/Bone_Mineral_Density.ipynb)

Workflows that include automatic contouring: 
* [Automatic contouring workflow based on an existing periosteal mask](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/ormir_xct/workflows/autocontour_gobj_workflow.py)
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
