# RIAWELC Welding Defect Classification

This project investigates lightweight CNN-based welding defect classification using the RIAWELC industrial welding dataset.

A customized SqueezeNet-based architecture was developed to analyze the trade-off between computational efficiency and classification performance for industrial visual inspection tasks.

---

# Project Overview

Automated welding defect inspection is an important problem in industrial quality control systems.

This project focuses on detecting welding defects from RGB welding images using a lightweight convolutional neural network architecture.

Instead of using large and computationally expensive CNN models, the project investigates whether a modified SqueezeNet architecture can achieve strong classification performance with lower parameter cost.

The system classifies welding images into four categories:

* Crack (CR)
* Porosity (PO)
* Lack of Penetration (LP)
* No Defect (ND)

---

# Proposed Architecture

The model is based on a pretrained SqueezeNet backbone.

A custom classification head was designed after the Fire9 module to improve representation capacity while preserving lightweight architecture advantages.

The custom head includes:

* 1×1 convolution layer
* Batch Normalization
* ReLU activation
* Global Average Pooling
* Dropout
* Fully Connected classification layer

The architecture was designed to balance:

* parameter efficiency,
* feature extraction capability,
* and industrial deployment feasibility.

---

# Training Pipeline

The training workflow includes:

1. Dataset preprocessing
2. Image resizing and normalization
3. Data augmentation
4. Transfer learning with pretrained SqueezeNet
5. Fine-tuning of custom classification head
6. Evaluation with confusion matrix and class-based metrics

---

# Dataset

Dataset: RIAWELC Welding Defect Dataset

Classes:

* Crack (CR)
* Porosity (PO)
* Lack of Penetration (LP)
* No Defect (ND)

The dataset contains industrial welding images collected for defect inspection research.

---

# Data Augmentation

To improve generalization performance, the following augmentations were applied:

* Random rotation
* Brightness adjustment
* Contrast adjustment

ImageNet normalization statistics were used during preprocessing.

---

# Optimization and Regularization

The following techniques were used to improve generalization:

* AdamW optimizer
* Dropout
* Batch Normalization
* Early stopping

---

# Results

## Final Performance

* Test Accuracy: 93.53%
* Macro F1-Score: 0.93

The experiments showed that the lightweight SqueezeNet-based architecture achieved strong classification performance despite having lower computational complexity compared to larger CNN models.

---

# Error Analysis

Confusion matrix analysis showed that:

* LP and CR classes occasionally overlap due to visual similarity,
* PO and ND classes were classified more consistently,
* lightweight architectures can still provide strong industrial inspection performance when combined with proper regularization and augmentation techniques.

---

# Repository Structure

```text
riawelc-welding-defect-classification/
│
├── report_outputs/
├── LICENSE
├── Proje Sunumu.pdf
├── Proje.ipynb
├── README.md
├── Rapor.pdf
└── requirements.txt
```

---

# Additional Materials

* `Rapor.pdf` contains the full project report.
* `Proje Sunumu.pdf` contains the presentation slides.
* `report_outputs/` contains experimental outputs, figures and evaluation results.

---

# Libraries and Tools

* PyTorch
* Torchvision
* NumPy
* Pandas
* Matplotlib
* scikit-learn

---

# Key Topics

* Computer Vision
* Deep Learning
* CNN
* SqueezeNet
* Industrial AI
* Welding Defect Detection
* Image Classification
* Transfer Learning

---

# Author

Emir Kaan SAIT

Yıldız Technical University
M.Sc. Computer Engineering
