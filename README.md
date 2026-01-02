RetinalFusionNet: A Dual-Branch Synergy Framework for Fine-Grained Retinal OCT Classification

![alt text](https://img.shields.io/badge/PyTorch-ee4c2c?logo=pytorch&logoColor=white)


![alt text](https://img.shields.io/badge/License-MIT-blue.svg)


![alt text](https://img.shields.io/badge/Accuracy-98.79%25-brightgreen.svg)


![alt text](https://img.shields.io/badge/Macro_AUC-0.9984-blue.svg)

This repository contains the official PyTorch implementation of RetinalFusionNet, a novel dual-branch synergy framework designed to bridge the gap between global pathological context and localized anatomical integrity in Optical Coherence Tomography (OCT) imaging.

🌟 Research Highlights

Peak Diagnostic Performance: Achieved a state-of-the-art (SOTA) accuracy of 98.79% and a Macro-AUC of 0.9984 on the Retinal OCT-C8 dataset.

Dual-Expert Synergy (V3+V4): Identified the optimal integration of a Specialist model (V3) for structural details and a Sprint-God model (V4) for global robustness.

Clinical Reliability: Reached a macro-average specificity of 99.83%, effectively minimizing the risk of false positives in medical screening.

Exceptional Stability: Validated through 100 independent training cycles with an extremely low variance of ±0.06%.

Interpretability: Utilizes high-resolution Grad-CAM visualizations to ensure model decisions align with actual anatomical lesions.

🏛 Framework Architecture

RetinalFusionNet integrates a Dual-Branch feature extraction strategy:

Semantic Branch: Uses a pre-trained ConvNeXt-Tiny to model holistic pathological representations.

Edge Branch: A dedicated sequential CNN to safeguard high-frequency topographic gradients and layer boundaries.

MSFA Module: A Multi-Scale Fusion Attention engine that adaptively adjudicates the information flow between branches via learnable gating (
𝜆
λ
).

![alt text](figures/Figure1_Architecture.png)

(Please upload your architecture diagram to the figures/ folder)

🛠 Installation & Setup
Prerequisites

Python 3.10+

CUDA 11.8+ (NVIDIA RTX 3060/4090 recommended)

Environment Setup
code
Bash
download
content_copy
expand_less
# Clone the repository
git clone https://github.com/kobayashi0512/RetinalFusionNet.git
cd RetinalFusionNet

# Install required dependencies
pip install -r requirements.txt
📊 Dataset Preparation

The model is trained and validated on standard benchmark datasets:

Internal Dataset (Retinal OCT-C8): 24,000 SD-OCT images across 8 diagnostic categories. Available on Kaggle.

External Dataset (OCT2017): Used for generalization verification. Available on Mendeley.

Sample Visualization:

![alt text](figures/figure2_oct_samples.png)

📂 Execution Pipeline
1. Training (V4 God-Tier Optimization)

To reproduce the 98.71% single-model performance using the Sprint configuration:

code
Bash
download
content_copy
expand_less
python scripts/ChoroDualNet_Sprint.py
2. Ultimate Ensemble & Evaluation

To run the Dual-Emperor (V3+V4) integration and generate the final metrics (98.79%):

code
Bash
download
content_copy
expand_less
python scripts/RetinalFusionNet_Final_Emperor_Evaluation.py
3. Exhaustive Ablation Search

To verify the synergy of all model combinations:

code
Bash
download
content_copy
expand_less
python scripts/RetinalFusionNet_Exhaustive_Ablation.py
📈 Key Results
Quantitative Metrics (Test Set)
Metric	Value	Achievement
Accuracy (Overall)	0.9879	98.79%
Macro-Average AUC	0.9984	Excellent Discriminative Power
Specificity	0.9983	Low Misdiagnosis Risk
Recall (Sensitivity)	0.9879	High Sensitivity
F1-Score	0.9879	Robust Performance
Stability Analysis (N=100)

![alt text](figures/Figure3_HighContrast_Stability.png)

📜 Data Availability & Funding
Data Availability

Source code, configuration files, and evaluation scripts are available in this repository. Datasets are sourced from public academic repositories (Kaggle/Mendeley).

Funding

This work was supported by the open research fund of the Key Laboratory of Computational Science and Application of Hainan Province (Grant No. JSKX202102).

Conflicts of Interest

The authors declare that they have no known competing financial interests or personal relationships that could have appeared to influence the work reported in this paper.

✉️ Contact

For questions regarding the methodology or code, please contact:
[Your Name] - [Your Email Address]

