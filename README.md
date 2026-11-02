# RetinalFusionNet

RetinalFusionNet is a dual-branch framework for structural and semantic feature fusion in retinal optical coherence tomography (OCT) image classification.

## Framework

- **Semantic Branch:** A ConvNeXt-Tiny backbone extracts contextual features from the OCT image.
- **Edge Branch:** A convolutional branch learns local structural features from an aligned intensity representation of the same preprocessed image. It is trained through the image-level classification objective.
- **Multi-Scale Feature Aggregation (MSFA):** The branch features are aligned, projected, and concatenated, then fused through convolution for classification.

The reported final model combines predictions from the V3 and V4 variants. The manuscript also reports architectural comparisons, loss ablation, and response visualizations.

## Datasets and reported results

| Evaluation | Accuracy | Macro AUC | Macro F1-score |
| --- | ---: | ---: | ---: |
| OCT-C8, eight-class test set | 98.79% | 0.9984 | 98.79% |
| OCT2017, four shared categories | 96.93% | 0.9956 | 95.84% |

- **OCT-C8:** [Retinal OCT Image Classification - C8](https://www.kaggle.com/datasets/obulisainaren/retinal-oct-c8).
- **OCT2017:** [Labeled OCT and Chest X-Ray Images for Classification, Version 2](https://data.mendeley.com/datasets/rscbjbr9sj/2). The evaluation uses the CNV, DME, drusen, and Normal categories shared with OCT-C8.

The manuscript describes the evaluation settings and the dataset image-overlap audit in its methods and limitations sections.

## Repository contents

- [`figure.zip`](figure.zip): figure archive.
- [`requirements.txt`](requirements.txt): dependency list.
- [`README.md`](README.md): project overview and data links.

Training scripts, evaluation scripts, and model weights are not present in the current public repository. The dependency list describes the environment and does not by itself provide a runnable implementation.

## Funding

This work was supported by the Fundamental Research Funds for the Provincial Universities of Liaoning under Grant No. LJ212410150016.

## Contact

For project-related questions, please use the repository's [Issues](https://github.com/kobayashi0512/RetinalFusionNet/issues).
