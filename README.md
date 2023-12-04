# Neural networks with divisive normalization for image segmentation

Official repository of the paper: [Neural networks with divisive normalization for image segmentation, Pattern Recognition Letters, 173](https://www.sciencedirect.com/science/article/pii/S0167865523002209).

## Introduction

One of the key problems in computer vision is adaptation: models are too rigid to follow the variability of the inputs. The canonical computation that explains adaptation in sensory neuroscience is divisive normalization, and it has appealing effects on image manifolds. In this work, we show that including divisive normalization in current deep networks makes them more invariant to non-informative image changes. 

## Results

U-Net type models with/without Divisive Normalization layers trained in the original Cityscapes dataset and evaluated in the Foggy Cityscapes data. The mean IoU results are:

| Dataset               |   No DN layers   |        1 DN layer        |      1-2 DN layers       |      1-3 DN layers       |      2-4 DN layers       |      1-4 DN layers       |
|:---------------------:|:----------------:|:------------------------:|:------------------------:|:------------------------:|:------------------------:|:------------------------:|
| Original Cityscapes   |  0.75 &pm; 0.02  |  0.75 &pm; 0.01 (0.0%)   |  0.76 &pm; 0.02 (1.3%)   |  0.77 &pm; 0.02 (2.7%)   |  0.77 &pm; 0.02 (2.7%)   |  0.77 &pm; 0.02 (2.7%)   |
| Low fog Cityscapes    |  0.65 &pm; 0.02  |  0.65 &pm; 0.04 (0.0%)   |  0.68 &pm; 0.02 (4.6%)   |  0.69 &pm; 0.02 (6.2%)   |  0.70 &pm; 0.03 (7.7%)   |  0.70 &pm; 0.02 (7.7%)   |
| Middle fog Cityscapes |  0.54 &pm; 0.03  |  0.53 &pm; 0.04 (-1.9%)  |  0.57 &pm; 0.03 (5.6%)   |  0.60 &pm; 0.03 (11.1%)  |  0.61 &pm; 0.03 (13.0%)  |  0.62 &pm; 0.03 (14.8%)  |
| High fog Cityscapes   |  0.40 &pm; 0.05  |  0.38 &pm; 0.04 (-5.0%)  |  0.41 &pm; 0.04 (2.5%)   |  0.46 &pm; 0.04 (15.0%)  |  0.49 &pm; 0.03 (22.5%)  |  0.48 &pm; 0.03 (20.0%)  |

## Conclusions

- Introducing divisive normalization layers in the encoding blocks leads to consistent improvements in IoU in the Cityscapes dataset.
- A model with divisive normalization trained only with images acquired in good weather conditions obtains a substantial increase in IoU over conventional U-Net when tested with images in bad weather conditions.
- The higher the level of fog introduced, the higher the advantage of the divisive normalization.

## Cite

@misc{hernandez_divisive_normalization_segmentation,
author = {Pablo Hernández-Cámara and Jorge Vila-Tomás and Valero Laparra and Jesús Malo},
title = {Neural networks with divisive normalization for image segmentation},
journal = {Pattern Recognition Letters},
volume = {173},
pages = {64-71},
year = {2023},
issn = {0167-8655},
doi = {https://doi.org/10.1016/j.patrec.2023.07.017},
url = {https://www.sciencedirect.com/science/article/pii/S0167865523002209}}

