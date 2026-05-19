# HCGAN_SMOKE_dataset

This repository contains the **SMOKE dataset** of unpaired forest-fire smoke images, along with a pseudo-paired test set **Fo-Haze**, created for image dehazing research using the **Haze-CycleGAN (HCGAN)** framework.

## Overview

Recent advances in image dehazing struggle to handle special scenarios like forest-fire smoke due to non-homogeneous haze and lack of paired data. To address this, **HCGAN** generates structurally aligned pseudo-paired hazy images from unpaired clear forest images and smoke images, preserving background structures while simulating realistic smoke patterns.

## Dataset

- **SMOKE**: Unpaired dataset containing:
  - 2,088 haze-free images
  - 2,303 hazy images
- **Fo-Haze**: Small pseudo-paired test set for supervised evaluation.
- Images are cropped to 256 × 256 pixels from original FLAME2 UAV videos. Manual screening was applied to improve haze-free image purity.

## Usage

This dataset can be used to:

- Train and evaluate image dehazing models in forest-fire scenarios
- Analyze cross-domain robustness of existing dehazing methods
- Benchmark pseudo-paired haze generation methods

## Reference

If you use this dataset, please cite:

```bibtex
@article{yourpaper2026,
  title={Unpaired Image-to-Image Translation for Paired Hazy Image Synthesis},
  author={Your Name et al.},
  journal={IEEE Transactions on Image Processing},
  year={2026},
  note={Preprint available on GitHub: https://github.com/feyadesu/HCGAN_SMOKE_dataset}
}
