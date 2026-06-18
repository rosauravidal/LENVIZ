[![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

# LENVIZ
[![WACV 2024](https://img.shields.io/badge/WACV_2024-CVF_Paper-00a896.svg)](https://openaccess.thecvf.com/content/WACV2026/html/Aithal_LENVIZ_A_High-Resolution_Low-Exposure_Night_Vision_Benchmark_Dataset_WACV_2026_paper.html)
[![paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2503.19804)
[![YouTube Video](https://img.shields.io/badge/YouTube-Video-red?logo=youtube&logoColor=white)](https://youtu.be/pDq2XlAdmZE)
[![GitHub](https://img.shields.io/badge/GitHub-View_Code-blue?logo=github)](https://github.com/rosauravidal/LENVIZ)
[![Hugging Face](https://img.shields.io/badge/Hugging_Face-Dataset-yellow?logo=huggingface)](https://huggingface.co/datasets/rosauravidal/LENVIZ)

Official Repo for the Low Exposure Night Vision (LENVIZ) Dataset, a comprehensive multi-exposure benchmark dataset for low-light image enhancement comprising of over 230K frames showcasing 24K real-world indoor and outdoor, with-and-without human, scenes.

![Teaser image](figures/teaser_figure.jpg)

## Data Overview
LENVIZ is a comprehensive multi-exposure benchmark dataset for low-light image enhancement. Traditional imaging systems struggle in low-illumination environments due to their limited dynamic range, increased noise, and reduced signal-to-noise ratios. To advance research in this field, this dataset provides over 230K frames showcasing 24K real-world indoor and outdoor scenes.

## Key Features of the Dataset
1. **Massive Scale and High Resolution**: The dataset comprises 234,688 total frames, making it the largest publicly available up-to 4K resolution benchmark in the field.
2. **Multi-Exposure Flexibility**: Each scene includes 9 distinct exposure frames alongside a long-exposure shot.
3. **Expert-Curated Ground Truth**: High-quality ground truth images are provided for 13,067 scenes. These were meticulously edited by a team of 7 expert photographers focusing on technical quality, including brightness, contrast, and noise reduction.
4. **ISP-Tuned Raw Data Simulation**: LENVIZ provides JPEG images that are exclusively ISP-tuned, devoid of any default camera post-processing. This captures the inherent noise, over-exposure, and artifacts characteristic of low-light conditions.
5. **Diverse Content and Subjects**: The dataset incorporates 14 mannequins spanning a diverse range of skin tones and facial features. Overall, 70% of the scenes contain one or more faces.

## Dataset Composition
1. **Training Dataset**: Captured using three distinct camera modules (S5K4H7YX03-FGX9, S5KJN1SQ03, and S5KJNS) to broaden representativeness.
   
| Camera Module | Resolution | Human GT (Files) | Human GT (Scenes) | Long Exposure GT (Files) | Long Exposure GT (Scenes) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| S5K4H7YX03-FGX9 | 3264x2448 | 81,099 | 7,487 | 72,947 | 7,862 |
| S5KJN1SQ03 | 4080x3072 | 39,972 | 4,009 | 22,132 | 3,023 |
| S5KJNS | 4080x3072 | 17,250 | 1,571 | 1,288 | 130 |
| **Total** | | **138,321** | **13,067** | **96,367** | **11,015** |

2. **Testing Dataset**: A curated set of 1,468 frames from 203 unique scenes. It is divided into a "Reference" partition, which includes 60 scenes with paired human-edited ground truth, and a "No-reference" partition, which includes 143 scenes with handheld captures and human subjects.
   
| Data-type | # of files | # of scenes |
| :--- | :--- | :--- |
| Reference | 610 | 60 |
| No-reference | 858 | 143 |
| **Total** | **1,468** | **203** |

## Benchmarked Models
The dataset was utilized to conduct an in-depth evaluation of current state-of-the-art low-light image enhancement techniques.
1. **Single Exposure Methods**: Evaluated models include LLFormer, ExpoMamba, and ZeroDCE++.
2. **Multi-Exposure Methods**: Evaluated models include MEFNet, HoLoCo, and MobileMEF.
3. **Performance**: Models trained on LENVIZ consistently achieved superior scores in perceptual metrics like LPIPS and SSIM, demonstrating the dataset is highly effective at training models to produce visually pleasing and structurally sound results.

## Terms of Use & Data License Agreement

The LENVIZ dataset is released under a [Creative Commons Attribution-NonCommercial 4.0 International License][cc-by-nc] 

[![CC BY-NC 4.0][cc-by-nc-image]][cc-by-nc]

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-image]: https://licensebuttons.net/l/by-nc/4.0/88x31.png
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg

1. **Training Dataset**: Publicly available on [Hugging Face](https://huggingface.co/datasets/rosauravidal/LENVIZ). No request is required.
2. **Test Dataset**: While this subset is available under the same CC BY-NC 4.0 license, it contains sensitive imagery (human faces). To ensure we have a record of users accessing this data, please request access via this form: [Access request](https://forms.gle/pVzCPtSGi91VZmGT8)

By downloading the training data or requesting access to the test dataset, the Applicant (hereafter "User") agrees to the terms outlined in the license.

## Bibtex
```
@InProceedings{Aithal_2026_WACV,
    author    = {Aithal, Manjushree and VidalMata, Rosaura G and Kartha, Manikandtan and Chen, Gong and Adhikarla, Eashan and Kirsten, Lucas Nedel and Fu, Zhicheng and Madhusudhana, Nikhil Ambha and Nasti, Joseph V.},
    title     = {LENVIZ: A High-Resolution Low-Exposure Night Vision Benchmark Dataset},
    booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},
    month     = {March},
    year      = {2026},
    pages     = {2531-2540}
}
```
