# Automatic contouring based on periosteal mask

The automatic contouring algorithm in the ORMIR_XCT package generates the periosteal mask of the distal and proximal bones of the wrist joint as well as a joint masking combining the distal and proximal bone masks. This variant of the autocontouring uses the gray value image as well as rough periosteal masks of the distal and proximal bones as input. It enables generation of the periosteal and joint masks when the distal and proximal bones are too close to each other (i.e. narrow joint space width) to distinguish.

## Function
```shell
To use automatic contouring with a gray value image and already present periosteal mask as input, use the following command:
autocontour_gobj(img, 
    dst_gobj, 
    prx_gobj):
```

## Input parameter settings
````{tab-set}
```{tab-item} HR-pQCT
`img`: SITK image or path to image   
`dst_gobj`: SITK image or path to distal mask   
`prx_gobj`: SITK image or path to proximal mask
```
````

## Examples and workflows
````{tab-set}
```{tab-item} HR-pQCT 
Examples of how to use the function for the automatic contouring based on a gray value image as input can be found in:
* [Automatic contouring example](tutorials/Autormatic_Countour.ipynb) 
* [Bone mineral density analysis example](tutorials/Bone_Mineral_Density.ipynb)

Workflows that include automatic contouring: 
* [Automatic contouring workflow using the mask (.gobj) as input](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/ormir_xct/workflows/autocontour_gobj_workflow.py)
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
