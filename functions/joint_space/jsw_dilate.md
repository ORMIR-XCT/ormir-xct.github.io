# Joint space image dilation

Joint space image dilation expands a three-dimensional binary joint segmentation using a ball structural unit. The function retains the largest connected component and fills holes within the dilated image.

## Function

To dilate the joint segmentation image, use the following function:

```shell
jsw_dilate(image)
```

## Input settings

````{tab-set}
```{tab-item} HR-pQCT 

`image`: Binary image of the joint segmentation  

Further information about the function and its inputs can be [here (tbd)]().
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

Examples of how to use joint space image dilation:
- [Finger_Joint_Comparison.ipynb](https://github.com/ORMIR-XCT/ormir-xct.github.io/blob/main/tutorials/Finger_Joint_Comparison.ipynb)

Workflows that include joint space image dilation:
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
> We used the method implemented in ORMIR-XCT [](https://doi.org/10.21105/joss.06084)

```

```{tab-item} PCD-CT

Coming soon
```

```{tab-item} µCT

Coming soon
```
````
