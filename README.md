# HCGAN dataset release

Forest smoke synthesis data associated with HCGAN.

Download the ZIP files from this repository's **Releases** page, not the automatically generated Source code archives.

| Archive | Contents |
|---|---|
| SMOKE_unpaired_training.zip | 1,888 clear images and 2,103 real smoke images for unpaired generator training |
| HCGAN_training_pairs.zip | 1,888 synthetic smoke/source pairs: 1,844 train pairs and 44 validation pairs |
| Fo_Haze_test_200.zip | 200 synthetic smoke/source test pairs from held-out videos 1 and 2 |

## Protocol
Generator training uses FLAME2 source videos 3–6. The downstream restoration split uses videos 3–5 for training and video 6 for validation. Fo-Haze refers to the held-out test set: 53 pairs from video 1 and 147 from video 2. Training pairs are supplied separately and are not additional Fo-Haze test samples.

Synthetic smoke images are generated; their references are the corresponding source images, not independently captured smoke-free counterparts of real smoke observations. The 200 test frames come from two videos, not 200 independent scenes.

Extract each ZIP into its own directory. Each archive includes a manifest with relative file paths and SHA-256 checksums. Match files using the manifest (extensions may differ between synthetic images and references). SHA256SUMS.txt contains archive checksums.

## Source attribution and reuse
Source imagery is derived from FLAME2. Original data rights and attribution requirements remain applicable. This package does not grant a new license over third-party imagery. Before public redistribution, the releasing authors should supply the original FLAME2 source URL, its applicable license/redistribution terms, and the accepted paper's citation. No blanket MIT license is assigned to the images.

This release excludes old random-frame test splits, Corsican augmentation data, comparison-method outputs, model weights, and local experiment logs.
