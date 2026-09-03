# Joint space image erosion

Joint space image erosion reduces a dilated three-dimensional binary joint segmentation using a ball structural unit. Connected-component analysis is then used to create the joint space mask and a dilated joint space mask.

## Function

To create the joint space masks, use the following function:

```shell
jsw_erode(dilated_image,
    pad_image)
```

## Input settings

````{tab-set}
```{tab-item} HR-pQCT 

`dilated_image`: Dilated binary image of the joint segmentation  
`pad_image`: Padded binary image of the joint segmentation  

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

Examples of how to use joint space image erosion:
- [Finger_Joint_Comparison.ipynb](https://github.com/ORMIR-XCT/ormir-xct.github.io/blob/main/tutorials/Finger_Joint_Comparison.ipynb)

Workflows that include joint space image erosion:
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
