# HCGAN: Forest-Fire Smoke Datasets

This repository provides the datasets used in our accepted paper on generating clear–smoke pseudo-pairs from unpaired forest imagery using HCGAN.

The release includes unpaired images for smoke synthesis training, synthetic pairs for supervised restoration, and the Fo-Haze test set.

## Download

| Dataset | Contents | Download |
|---|---|---|
| SMOKE unpaired training data | 1,888 clear images and 2,103 real smoke images | [Download ZIP](https://github.com/feyadesu/HCGAN_SMOKE_dataset/releases/download/v1.0.0/SMOKE_unpaired_training.zip) |
| HCGAN training pairs | 1,888 synthetic smoke/source pairs: 1,844 training pairs and 44 validation pairs | [Download ZIP](https://github.com/feyadesu/HCGAN_SMOKE_dataset/releases/download/v1.0.0/HCGAN_training_pairs.zip) |
| Fo-Haze test set | 200 synthetic smoke/source pairs from held-out videos | [Download ZIP](https://github.com/feyadesu/HCGAN_SMOKE_dataset/releases/download/v1.0.0/Fo_Haze_test_200.zip) |

The datasets are provided as attachments on the [Releases page](https://github.com/feyadesu/HCGAN_SMOKE_dataset/releases/tag/v1.0.0). The automatically generated “Source code” archives do not contain the image datasets.

Archive checksums are available in [SHA256SUMS.txt](SHA256SUMS.txt).

## Dataset Construction and Splits

### Unpaired generator training

HCGAN is trained using 1,888 clear images and 2,103 real smoke images from FLAME2 source videos 3–6. The two image domains are unpaired.

### Supervised restoration pairs

Each synthetic training pair consists of an HCGAN-generated smoke image and its corresponding clear source image.

The 1,888 pairs are divided by source video for downstream restoration experiments:

- Training: 1,844 pairs from videos 3–5.
- Validation: 44 pairs from video 6.

### Fo-Haze test set

Fo-Haze contains 200 test pairs constructed from held-out source videos:

- Video 1: 53 pairs.
- Video 2: 147 pairs.

The generator-training and Fo-Haze test partitions do not share source videos. Fo-Haze refers specifically to these 200 test pairs; the 1,888 training and validation pairs are provided separately.

The smoke images in these pairs are synthetic, and their references are the corresponding clear source images. They are not independently captured clear–real-smoke pairs. The test set contains frames from two videos rather than 200 independent scenes.

## File Organization

Extract each archive into a separate directory.

### SMOKE_unpaired_training.zip

```text
train/
├── clear/
└── real_smoke/
manifest.csv
