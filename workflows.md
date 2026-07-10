# Workflows

```mermaid

%%{init:{
 "theme":"base",
 "flowchart":{
 "nodeSpacing":40,
 "rankSpacing":40
 }
}}%%

flowchart LR

    subgraph PP["Pre-Processing"]
        direction TB
        G["Gaussian"]
        LH["Laplace-Hamming"]
        G ~~~ LH
    end

    subgraph SEG["Segmentation"]
        direction TB
        A["Automatic Contouring"]
        LA["Local Adaptive<br/>Threshold"]
        A ~~~ LA
    end

    subgraph ANA["Analysis"]
        direction TB
        subgraph JS["Joint Space Analyses"]
            direction LR
            W["Joint Space<br/>Width"]
            V["Joint Space<br/>Volume"]
            W ~~~ V
        end
        subgraph BMD["Bone Mineral Density"]
            direction TB
            B["BMD"]
        end
        subgraph T["Trabecular Bone Analyses"]
            TM["Trabecular<br/>Microarchitecture"]
            TBV["Trabecular Bone<br/>Volume Fraction"]
            TT["Trabecular<br/>Thickness"]
            TS["Trabecular<br/>Spacing"]
            direction LR
            TM ~~~ TBV
            TS ~~~ TT
        end
        T ~~~ JS
    end

    PP --> SEG --> ANA

    classDef preprocess fill:#1E88E5,stroke:#1565C0,color:#ffffff;
    class G,LH preprocess;
    
    classDef segmentation fill:#D81B60,stroke:#333333,color:#ffffff;
    class A,LA segmentation;
    
    classDef analyses fill:#FFC107,stroke:#333333,color:#000000;
    class W,V,B,TM,TBV,TT,TS analyses
    
    classDef boxText font-size:20px;
    class PP,SEG,ANA boxText;
    
    classDef SubBoxText font-size:15px,font-weight:bold;
    class JS,BMD,T SubBoxText;
    
    classDef largeText font-size:15px;
    class G,LH,A,LA,W,V,B,TM,TBV,TT,TS largeText;

```

## Prerequisites

**Please see below for general pre-requisites for running workflows**

Install the package below so console scripts are available:

```bash
pip install -e .
```

After this, run any workflow by script name:
```bash
<workflow_name.py> -h
```

## Current Workflows

### Bone segmentation

- [Segmentation](workflows/modules/segmentation/segmentation_modules.md)

### Morphology-Based Measurements

- [Morphology](workflows/modules/morphology/morphology_modules.md)

### Bone Mineral Density (BMD) techniques

- [Bone Mineral Density](workflows/modules/bmd/bmd_modules.md)


