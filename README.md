# IPMDNet

<p align="center">
  <img src="https://img.shields.io/badge/Research-Interpretability-blue" alt="Research Interpretability" />
  <img src="https://img.shields.io/badge/Task-Retinal%20Vessel%20Segmentation-green" alt="Retinal Vessel Segmentation" />
  <img src="https://img.shields.io/badge/Domain-Multimodal%20Medical%20Imaging-orange" alt="Multimodal Medical Imaging" />
</p>

IPMDNet: Interpretably Pruned Magnification-Demagnification Network for Multimodal Retinal Image Segmentation.

## Overview

This repository contains the implementation and experimental notebook for IPMDNet, an interpretable and lightweight deep learning framework for multimodal retinal vessel segmentation. The work focuses on accurate segmentation of thin and small retinal vessels in resource-constrained settings while preserving model transparency and reducing computational cost.

The project is built around a lightweight Magnification-Demagnification Network (MDNet), which extracts fine vessel structures by magnifying intermediate feature maps during feature extraction and demagnifying them during reconstruction. To improve efficiency and interpretability, the model is further refined using Layer-wise Segmentation Contribution Score (LSCS), which quantifies how much each hidden layer contributes to the final segmentation performance. Non-contributory layers are then pruned through a structured pruning strategy.

## Research Abstract

Structural and functional alterations in retinal blood vessels are emerging as potential biomarkers for early detection and diagnosis of systemic diseases during asymptomatic stages. Accurate retinal vessel segmentation is therefore crucial for enabling early disease diagnosis. While deep learning (DL) models have demonstrated significant success in automatic retinal vessel segmentation, challenges related to interpretability and over-parameterization limit their deployment in resource-constrained environments.

To address these limitations, we proposed an interpretably pruned magnification-demagnification network (IPMDNet) for segmenting blood vessels in multimodal retinal images. To develop IPMDNet, we primarily designed a DL-based light-weight magnification demagnification network (MDNet) for accurate segmentation of small and fine retinal vessels. Unlike conventional DL-based segmentation models, MDNet magnifies feature maps during feature extraction and demagnifies them during feature reconstruction to produce accurate segmented outputs. Despite containing only 0.33 million parameters, this model achieved comparative performance against state-of-the-art models having significantly higher parameters across six multimodal retinal vessel datasets.

To interpret the MDNet model's segmentation performance, we have also developed a novel method for measuring Layer-wise Segmentation Contribution Score (LSCS) of deep hidden layers, which enables the visualization and quantification of their contributions to overall performance. Based on these interpretability scores, we perform structured pruning to eliminate non-contributory layers from our MDNet, resulting in our final IPMDNet model with 0.08 million parameters. The pruned model (IPMDNet) reduces approximately 75% of the parameters and nearly 93% of the computational complexity, while still achieving comparative segmentation performance against the original MDNet model, making the IPMDNet model particularly suitable for deployment in resource-constrained environments.

## Key Contributions

- Lightweight magnification-demagnification segmentation architecture for retinal vessel extraction
- Explicit focus on fine and small vessel segmentation, which is often challenging in retinal imaging
- Layer-wise Segmentation Contribution Score (LSCS) for model interpretability
- Structured pruning guided by interpretability to reduce model size and compute efficiently
- Comparative performance on six multimodal retinal vessel datasets despite a much smaller model
- Suitable deployment in resource-constrained clinical and research settings

## Model Motivation

Retinal vessels are important biomarkers for many systemic diseases, including diabetic retinopathy, glaucoma, and cardiovascular disorders. Early and accurate segmentation of retinal blood vessels is therefore crucial for screening, diagnosis, and disease monitoring. However, conventional deep learning segmentation models often require large parameter counts and are difficult to interpret, limiting their applicability in practical deployment scenarios.

IPMDNet addresses these problems by combining:

1. a compact segmentation backbone (MDNet),
2. magnification-based feature enhancement for small structures, and
3. pruning guided by interpretable contribution analysis.

This yields a model that is both efficient and transparent while maintaining strong segmentation performance.

## Repository Contents

This repository currently contains the full experimental notebook and project documentation:

```text
IPMDNet/
├── README.md
├── IPMDNet (All Files).ipynb
└── (additional files may be added in future revisions)
```

The main notebook includes the experiment workflow for the project, including model implementation, data processing, training/evaluation, and the interpretability-driven pruning analysis.

## Installation

Clone the repository:

```bash
git clone https://github.com/Sufianlab/IPMDNet.git
cd IPMDNet
```

Create and activate a Python environment:

```bash
python -m venv venv
source venv/bin/activate   # Linux/macOS
# or
venv\Scripts\activate      # Windows
```

Install the required dependencies. The exact environment may vary depending on the notebook and local setup, but a typical scientific Python stack includes:

```bash
pip install torch torchvision numpy pandas matplotlib scikit-learn opencv-python
```

## Usage

The project is primarily presented as a notebook-based implementation. To reproduce or extend the work:

1. Open `IPMDNet (All Files).ipynb` in Jupyter Notebook or Google Colab.
2. Run the cells in order to load the data, build the model, train/evaluate the network, and analyze LSCS-based pruning.
3. Adjust dataset paths, training parameters, or pruning ratios as needed for your experiments.

## Dataset and Evaluation

The method is designed for multimodal retinal vessel segmentation and was evaluated across six retinal vessel datasets in the reported work. The notebook in this repository contains the experimental pipeline used to explore this setting.

Researchers can adapt the notebook to use their preferred retinal vessel datasets and segmentation benchmarks.

## Expected Outcomes

- Accurate segmentation of small and fine retinal vessels
- A compact network suitable for low-resource settings
- Reduced model complexity through interpretability-guided pruning
- Better transparency in how hidden layers contribute to vessel segmentation

## Citation

Please cite this work when using the method or reproducing the experiments. If you are preparing a manuscript, use the paper title and abstract details above and include the official paper metadata once available.

```bibtex
@article{IPMDNet2026,
  title={IPMDNet: Interpretably Pruned Magnification-Demagnification Network for Multimodal Retinal Image Segmentation},
  author={Anonymous/To be completed},
  journal={Preprint / Journal Details TBD},
  year={2026}
}
```

## Contact

For questions, collaboration requests, or dataset access, please contact the maintainer or repository owner.

---

This README has been updated to match the manuscript abstract and the project notebook's focus on interpretable, lightweight multimodal retinal vessel segmentation.
