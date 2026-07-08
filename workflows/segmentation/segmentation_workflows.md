# Segmentation Workflows

This file documents the workflow entry points registered in `pyproject.toml` under `[project.scripts]`.

## Prerequisites

Install the package so console scripts are available:

```bash
pip install -e .
```

Then run any workflow by script name:

```bash
<workflow_name> -h
```

## `autocontour`

- [Automatic Contouring](autocontour_workflow.py)

Runs automatic contouring and writes three masks beside the input image.

```bash
autocontour IMAGE_PATH [--mu_water MU_WATER] [--rescale_slope RESCALE_SLOPE] [--rescale_intercept RESCALE_INTERCEPT]
```

- `IMAGE_PATH` (required): input image path
- `--mu_water` (optional, default `0.2409`)
- `--rescale_slope` (optional, default `1603.51904`)
- `--rescale_intercept` (optional, default `-391.209015`)

Outputs (same folder as input basename):
- `*_MASK.nii`
- `*_PRX_MASK.nii`
- `*_DST_MASK.nii`

Example:

```bash
autocontour sample.nii --mu_water 0.2409 --rescale_slope 1603.51904 --rescale_intercept -391.209015
```

## `autocontour_gobj`

- [Automatic Contouring (Distal/Proximal GOBJ Contours)](autocontour_gobj_workflow.py)

Runs autocontour using distal/proximal GOBJ contours as guidance.

```bash
autocontour_gobj IMAGE_PATH DST_GOBJ_PATH PRX_GOBJ_PATH
```

- `IMAGE_PATH`: input image path
- `DST_GOBJ_PATH`: distal contour GOBJ path
- `PRX_GOBJ_PATH`: proximal contour GOBJ path

Outputs:
- `*_MASK.nii`
- `*_PRX_MASK.nii`
- `*_DST_MASK.nii`

Example:

```bash
autocontour_gobj sample.nii sample_dst.gobj sample_prx.gobj
```

## `fft_laplace`

- [FFT Laplace](fft_laplace_hamming_workflow.py)

Runs Laplace-Hamming based segmentation and writes the output image.

```bash
fft_laplace INPUT_IMAGE OUTPUT_PATH [--upper UPPER] [--lower LOWER]
```

- `INPUT_IMAGE` (required)
- `OUTPUT_PATH` (required)
- `--upper` (optional): upper threshold
- `--lower` (optional): lower threshold

If thresholds are omitted, internal defaults in `segmentation_laplace_hamming` are used.

Examples:

```bash
fft_laplace sample.nii sample_fft_seg.nii
fft_laplace sample.nii sample_fft_seg.nii --lower 120 --upper 1000
```

## `gauss_seg`

- [Gaussian segmentation](seg_gauss_workflow.py)

Binarizes an image using the standard Gaussian segmentation protocol.

```bash
gauss_seg INPUT_IMAGE OUTPUT_IMAGE [--image_units IMAGE_UNITS]
```

- `INPUT_IMAGE` (required)
- `OUTPUT_IMAGE` (required)
- `--image_units` (optional, default `BMD`): one of `BMD`, `SCANCO`, `ATTENUATION`, `HU`, `PER1000`

Example:

```bash
gauss_seg sample.nii sample_seg.nii --image_units BMD
```

## `local_adaptive_threshold`

- [Local Adaptive Thresholding](adaptive_local_threshold_workflow.py)

Performs adaptive local threshold segmentation.

```bash
local_adaptive_threshold INPUT OUTPUT [options]
```

Required:
- `INPUT`: input image
- `OUTPUT`: output segmented image

Options:
- `--lower-threshold`, `-lt` (default `190`)
- `--upper-threshold`, `-ut` (default `450`)
- `--structuring-element-size`, `-sz` (default `6`)
- `--structuring-element-shape`, `-sh` (default `ball`, choices: `ball`, `cube`)
- `--sigma`, `-sg` (default `None`)
- `--minimum-structure-size`, `-ms` (default `64`)
- `--local-threshold-method`, `-ltm` (default `mean`, choices: `mean`, `minmax`, `both`)

Example:

```bash
local_adaptive_threshold sample.nii sample_local_seg.nii -lt 190 -ut 450 -sh ball -sz 6
```

