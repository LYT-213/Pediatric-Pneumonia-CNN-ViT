# Comparison of CNNs and Vision Transformers for Pediatric Pneumonia Screening

This repository contains the official PyTorch implementation for the manuscript: **"Comparison of CNNs and Vision Transformers for Pediatric Pneumonia Screening: A Multi-Center Cross-Domain Evaluation"**.

## 📊 Overview
This study evaluates the robustness and interpretability of three architectures (EfficientNet-B0, ConvNeXt-Tiny, ViT-Base-16) across:
*   **Training**: Adult data (CheXpert).
*   **Testing**: Three pediatric datasets (Kaggle, NIH, VinDr).
*   **Analysis**: Performance stability (N=5 seeds), sensitivity analysis, and quantitative XAI (Gini/Entropy).

## 📂 Repository Structure

| File | Description |
| :--- | :--- |
| `data/chexpert_20k_balanced.csv` | Metadata ensuring exact reproducibility of training splits. |
| `01_train_model.ipynb` | Training pipeline with fixed random seeds and automatic logging. |
| `02_evaluate_benchmark.ipynb` | Generates **Table 2** (F1, AUC, Sensitivity) using Paired t-tests. |
| `03_generate_figure2_xai.ipynb` | Generates **Figure 2** (Comprehensive XAI with LIME & Score-CAM). |
| `04_generate_figure3_cmp.ipynb` | Generates **Figure 3** (Side-by-side Attention Comparison). |
| `05_table3_xai_metrics.ipynb` | Generates **Table 3** (Quantitative Gini & Entropy metrics). |

## 🚀 Usage Guide

### 1. Environment Setup
To ensure compatibility with the XAI libraries (Grad-CAM/LIME), strict version requirements are enforced (e.g., `numpy<2`).
```bash
pip install -r requirements.txt