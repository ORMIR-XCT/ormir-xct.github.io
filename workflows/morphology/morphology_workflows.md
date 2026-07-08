# Morphology Measurement Workflows

This page contains Python files for running morphology-related workflows (e.g. measuring trabecular thickness, joint space width). Default inputs are listed for all of these files below.

## Prerequisites

Install the package so console scripts are available:

```bash
pip install -e .
```

Then run any workflow by script name:

```bash
<workflow_name> -h
```



## `jsw_main`

- [Joint Space Width Analysis](jsw_analysis_workflow.py)

Runs the joint-space-width (JSW) analysis pipeline on a binary joint segmentation.

```bash
jsw_main JOINT_SEG
```

- `JOINT_SEG`: joint segmentation image

Outputs (same directory as input):
- `*_DILATE.nii`
- `*_ERODE.nii`
- `*_JS_MASK.nii`
- `*_DILATED_JS_MASK.nii`
- `*_DT.nii`
- JSW parameter text output (written by `jsw_parameters`)

Example:

```bash
jsw_main joint_mask.nii
```

## `Trabecular (Tb) Microarchitecture`

- [Trabecular Microarchitecture](trab_microarchitecture_workflow.py)

**🚧 Workflow under construction 🚧**

## `Tb.TV/BV`

- [Trabecular Bone Volume Fraction](trab_bvtv_workflow.py)

**🚧 Workflow under construction 🚧**

## `Tb.Th`

- [Trabecular Thickness](trab_th_workflow.py)

**🚧 Workflow under construction 🚧**

## `Tb.Spacing`

- [Trabecular Spacing](trab_sp_workflow.py)

**🚧 Workflow under construction 🚧**
