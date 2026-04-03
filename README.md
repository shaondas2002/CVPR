# CVPR
CNN and ResNet18 based classification of leukemia cells (ALL vs HEM) using C-NMC dataset
# Leukemia Cell Classification using CNN and Transfer Learning

## Course
Computer Vision and Pattern Recognition – Midterm Assignment

## Overview
This project classifies microscopic blood cell images into two classes:
- ALL (Acute Lymphoblastic Leukemia)
- HEM (Healthy cells)

The work compares a baseline CNN, a regularized CNN, and a ResNet18 transfer learning model on the C-NMC leukemia dataset.

## Dataset
- **Name:** C-NMC Leukemia Dataset
- **Source:** https://www.kaggle.com/datasets/avk256/cnmc-leukemia
- **Classes:** 2 (ALL, HEM)

## Data Split
- **Training images:** 6631
- **Validation images:** 2057
- **Testing images:** 1973

## Models Used
1. Baseline Custom CNN
2. Custom CNN with Batch Normalization and Dropout
3. ResNet18 Transfer Learning

## Training Setup
- **Best model:** ResNet18 transfer learning
- **Learning rate:** 0.001
- **Regularization used:** Dropout
- **Trainable parameters:** 11177538
- **Best epoch:** 4
- **Epochs trained:** 7

## Best Results
- **Best validation accuracy:** 85.76%
- **Best validation loss:** 0.3694
- **Test accuracy:** 79.52%
- **Macro F1-score:** 0.7451
- **ROC-AUC:** 0.7811

## Class-wise Test Performance
| Class | Precision | Recall | F1-score |
|------|-----------|--------|----------|
| ALL  | 0.7869    | 0.9436 | 0.8581   |
| HEM  | 0.8262    | 0.5118 | 0.6321   |

## Observations
- The dataset is imbalanced, with more ALL images than HEM images.
- The model performs better on ALL than HEM.
- Weighted sampling was used in the ResNet18 experiment to reduce class imbalance effects.
- Transfer learning performed better than the custom CNN models.

## Visualizations

 -Confusion Matrix

 -ROC Curve

 -Training Curves

## Conclusion
ResNet18 transfer learning achieved the best performance among all tested models. The results show that transfer learning is effective for medical image classification on the C-NMC leukemia dataset, although class imbalance still affects HEM recall.
