<div align="center">

# Skin Cancer Diagnosis Using Transfer Learning

**A deep learning classifier that distinguishes Basal Cell Carcinoma, Melanoma, and Nevus from dermoscopic images, built on a fine-tuned MobileNetV2.**

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![MobileNetV2](https://img.shields.io/badge/Model-MobileNetV2-lightgrey)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

</div>

---

## Table of Contents

- [Overview](#overview)
- [Highlights](#highlights)
- [Sample Images by Class](#sample-images-by-class)
- [Dataset](#dataset)
- [Results](#results)
  - [Classification Report](#classification-report)
  - [Confusion Matrix](#confusion-matrix)
  - [ROC Curves](#roc-curves)
- [Acknowledgments](#acknowledgments)

---

## Overview

| | |
|---|---|
| **Domain** | Computer Vision, Machine Learning |
| **Sub-Domain** | Deep Learning, Image Recognition |
| **Techniques** | Deep Convolutional Neural Network, Transfer Learning (MobileNetV2) |
| **Application** | Image Recognition, Image Classification, Medical Imaging |

---

## Highlights

- Classifies three types of skin lesions from dermoscopic images using transfer learning on MobileNetV2
- Customized architecture, fine-tuned specifically for this three-class problem
- Strong performance across all three classes — see [Results](#results) below
- Built on the [ISIC 2019 Challenge](https://challenge.isic-archive.com/data/) dataset

---

## Sample Images by Class

<table>
  <tr>
    <td align="center" width="33%">
      <img src="images/Basal_cell_carcinoma.jpg" width="260"/><br/>
      <sub><b>Basal Cell Carcinoma</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="images/Melanoma.jpg" width="260"/><br/>
      <sub><b>Melanoma</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="images/Nevus.jpg" width="260"/><br/>
      <sub><b>Nevus</b></sub>
    </td>
  </tr>
</table>

---

## Dataset

**Source:** [ISIC Skin Cancer Challenge 2019](https://challenge.isic-archive.com/data/)

| | |
|---|---|
| **Dataset name** | ISIC Skin Cancer Images (Basal Cell Carcinoma vs Melanoma vs Nevus) |
| **Number of classes** | 3 |
| **Classes** | Basal Cell Carcinoma, Melanoma, Nevus |

---

## Results

### Classification Report

<p align="center">
  <img src="images/ACC.png" alt="Classification report: precision, recall, f1-score per class" width="500"/>
</p>

### Confusion Matrix

<p align="center">
  <img src="images/Confusion.png" alt="Confusion matrix across all three classes" width="480"/>
</p>

### ROC Curves

**Combined ROC (all classes with micro/macro average)**

<p align="center">
  <img src="images/ROC.png" alt="Combined ROC curve" width="520"/>
</p>

**Per-Class Breakdown**

<sub>Labeled based on the alphabetical class ordering visible in the classification report and confusion matrix above (Keras's default when class names aren't explicitly passed). Verify against the training script's `CLASS_NAMES` order if these figures came from a different run.</sub>

<table>
  <tr>
    <td align="center" width="33%">
      <img src="images/ROC_CLASS_0.png" width="260"/><br/>
      <sub><b>Basal Cell Carcinoma</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="images/ROC_CLASS_1.png" width="260"/><br/>
      <sub><b>Melanoma</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="images/ROC_CLASS_2.png" width="260"/><br/>
      <sub><b>Nevus</b></sub>
    </td>
  </tr>
</table>

---

## Acknowledgments

Built on the [ISIC 2019 Challenge](https://challenge.isic-archive.com/data/) dataset, 
licensed under [CC-BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).

Please cite the ISIC Archive and the underlying source datasets 
(HAM10000, BCN_20000, MSK) if you use this work or the dataset it is built on:

> Tschandl P., Rosendahl C. & Kittler H. The HAM10000 dataset, a large collection 
> of multi-source dermatoscopic images of common pigmented skin lesions. 
> Sci. Data 5, 180161 (2018).
>
> Codella N. et al. Skin Lesion Analysis Toward Melanoma Detection: A Challenge 
> at the 2017 ISBI, Hosted by ISIC. arXiv:1710.05006 (2017).
>
> Hernández-Pérez C. et al. BCN20000: Dermoscopic lesions in the wild. 
> Scientific Data 11, 641 (2024).

**Note:** This dataset is licensed for non-commercial use only. The trained model 
in this repository inherits that restriction.
