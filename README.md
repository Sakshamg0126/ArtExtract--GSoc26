# ArtExtract--GSoc26
A multi-task PyTorch computer vision model using EfficientNet-V2 to simultaneously predict the artist and art type of classical artworks, featuring mathematical uncertainty metrics (Entropy &amp; Logit Deviation).
# 🏛️ AI Art Appraiser: Rijksmuseum Multi-Task Classifier

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

A professional-grade computer vision pipeline that analyzes classical artworks to predict both the **Artist** and the **Art Type** (e.g., painting, drawing, print). Built with PyTorch and an `EfficientNet-V2-S` backbone, this project demonstrates multi-task learning and advanced uncertainty metrics on the Rijksmuseum dataset.

## ✨ Key Features
* **Multi-Task Learning:** A single EfficientNet-V2 backbone splitting into two distinct classification heads to predict artist and art type simultaneously.
* **Smart Data Pipeline:** Utilizes a custom PyTorch `Dataset` with `TrivialAugmentWide` for robust, art-friendly data augmentation.
* **Mathematical Inference Metrics:** Beyond simple predictions, the inference script calculates:
  🎯 PREDICTION RESULTS
* Top Confidence: 0.8942 (89.42%).
* Mean Score:     -0.0124.
* Mean Deviation: 0.9452.
* Entropy Loss:   0.4120.
* **Production-Ready Structure:** Modular code design separating data loading, model architecture, training, and inference.

## 📊 The Dataset
This project uses the [Rijksmuseum Dataset](https://www.kaggle.com/datasets/lgmoneda/rijksmuseum) from Kaggle. It contains digitized, high-resolution heritage artworks from the Dutch National Museum.
* **Imbalanced Data Handling:** The training loop utilizes `CrossEntropyLoss` with `label_smoothing=0.1` to prevent overconfidence on majority classes (like anonymous prints).

## 🚀 Getting Started

### 1. Prerequisites
Ensure you have Python 3.8+ and the following libraries installed:
```bash
pip install torch torchvision pandas scikit-learn pillow matplotlib tqdm kaggle
