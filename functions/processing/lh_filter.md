# Laplace-Hamming filter

Laplace-Hamming (LH) filtering is an edge-enhancing filtering approach. It combines a Laplace operator, which highlights edges and rapid intensity changes in an image, with a Hamming window, which limits high-frequency noise in an image.

## Function
To use the LH filter combined with a fixed threshold, use the following commands:
```python
from ormir_xct.core.segmentation.fft_laplace_hamming import fft_laplace_hamming

fft_laplace_hamming(
    image_np, 
    laplace_epsilon, 
    lp_cut_off_freq, 
    hamming_amp)
```

## Input settings
````{tab-set}
```{tab-item} HR-pQCT

`image_np`: Gray value input image  
`laplace_epsilon`: Weight of the curvature image. Default = `0.45`   
`lp_cut_off_freq`: Low-pass cutoff frequency of the Hamming filter. Default = `0.3`   
`hamming_amp`: Amplitude of the Hamming filter. Default = `1.0`  

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

Examples of how to use the LH filter:
* [LH filtering example](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/examples/Laplace_Hamming_Filter.ipynb)

Workflows that include the LH filter:
* [Laplace-Hamming based global segmentation](https://github.com/ORMIR-XCT/ORMIR-XCT/blob/main/ormir_xct/workflows/adaptive_local_threshold_workflow.py)
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

If you use this function, please cite it as follows:
> We used the Laplace-Hamming filter as implemented in ORMIR-XCT (@https://doi.org/10.21105/joss.06084).
```

```{tab-item} PCD-CT
Coming soon
```

```{tab-item} µCT
Coming soon
```
````