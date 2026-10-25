# IPMDNet

<p align="center">
  <img src="https://img.shields.io/badge/Research-Interpretability-blue" alt="Research Interpretability" />
  <img src="https://img.shields.io/badge/Task-Retinal%20Segmentation-green" alt="Retinal Segmentation" />
  <img src="https://img.shields.io/badge/Domain-Multimodal%20Medical%20Imaging-orange" alt="Multimodal Medical Imaging" />
</p>

IPMDNet: Interpretably Pruned Magnification-Demagnification Network for Multimodal Retinal Image Segmentation.

## Overview

This repository contains the implementation and supporting materials for IPMDNet, a deep learning framework designed for multimodal retinal image segmentation. The model is built to improve segmentation accuracy while preserving interpretability through a pruning-based magnification–demagnification design. The method is particularly relevant for retinal disease analysis, where precise vessel and lesion segmentation are critical for clinical decision-making.

## Research Abstract

Retinal image segmentation plays a crucial role in the early diagnosis and monitoring of ophthalmic diseases such as diabetic retinopathy, glaucoma, and age-related macular degeneration. However, conventional segmentation models often struggle to capture fine anatomical structures and multimodal features while maintaining interpretability. In this work, we propose IPMDNet, an Interpretably Pruned Magnification-Demagnification Network for Multimodal Retinal Image Segmentation. The proposed framework integrates multi-scale feature learning with a magnification-demagnification strategy to enhance representation of subtle retinal structures while suppressing redundant information. To improve efficiency and transparency, we introduce an interpretability-guided pruning mechanism that removes less useful components while preserving clinically meaningful features. Extensive experiments on multimodal retinal datasets demonstrate that IPMDNet achieves strong segmentation performance, improved robustness, and better model interpretability compared with existing approaches. The results suggest that the proposed method is a promising solution for reliable and explainable retinal image analysis in medical imaging applications.

## Key Contributions

- Multimodal retinal image segmentation framework
- Magnification–demagnification learning strategy for enhanced feature extraction
- Interpretability-guided pruning for compact and transparent network design
- Improved segmentation quality for clinically relevant retinal structures
- Suitable for research and clinical decision support workflows

## Motivation

Accurate segmentation of retinal structures from multimodal imaging data is essential for disease diagnosis and treatment planning. Traditional deep learning methods often sacrifice interpretability in favor of performance. IPMDNet addresses this challenge by combining strong representation learning with transparent, structure-aware design.

## Repository Structure

```text
IPMDNet/
├── README.md
├── data/                  # Dataset scripts and instructions
├── models/                # Model definitions
├── notebooks/             # Experimental notebooks
├── scripts/               # Training and evaluation scripts
├── src/                   # Source code
├── utils/                 # Helper functions and utilities
├── requirements.txt       # Python dependencies
├── LICENSE                # License information
└── results/               # Saved predictions and experiments
```

## Installation

1. Clone the repository

```bash
git clone https://github.com/Sufianlab/IPMDNet.git
cd IPMDNet
```

2. Create a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate   # Linux/macOS
# or
venv\Scripts\activate      # Windows
```

3. Install dependencies

```bash
pip install -r requirements.txt
```

## Usage

Training and evaluation instructions can be added here once the project code is uploaded.

```bash
python train.py --config configs/config.yaml
```

## Dataset

This project is designed for multimodal retinal image segmentation. Please prepare your dataset in the structure required by the training pipeline and update the relevant configuration files before running experiments.

## Expected Outcomes

- Better delineation of retinal lesions and anatomical structures
- Improved model interpretability
- More efficient network design through pruning-based optimization

## Citation

If you use this work in your research, please cite the paper appropriately.

```bibtex
@article{yourpaper2025,
  title={IPMDNet: Interpretably Pruned Magnification-Demagnification Network for Multimodal Retinal Image Segmentation},
  author={Author Names},
  journal={Journal Name},
  year={2025}
}
```

## Contact

For questions or collaboration requests, please contact the repository owner or maintainers.

## Notes

This README is structured to present the project in a professional and publication-ready format. If you want, the next step is to add the actual implementation files, notebook (.ipynb or .py), and the official paper title/authors once they are available.

---

If you want, I can also help you:
- add a polished `Abstract` section tailored to the exact paper wording,
- create a proper `requirements.txt`,
- generate a project folder structure for the code,
- or prepare a complete GitHub-ready README with your actual paper information and dataset details.
