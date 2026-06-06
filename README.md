# ♻️ Attention-Enhanced CNNs for Real-Time Multi-Class Waste Classification

## 📌 Overview

This project presents an intelligent waste classification system that automatically categorizes waste materials from both **land-based** and **underwater environments** using Deep Learning and Computer Vision techniques.

The system evaluates multiple pre-trained Convolutional Neural Network (CNN) architectures and enhances their performance using the **Convolutional Block Attention Module (CBAM)**. The best-performing model is deployed through a user-friendly web application for real-time waste classification.

---

## 🎯 Objectives

* Automate waste classification using image-based deep learning models.
* Improve classification performance using attention mechanisms.
* Handle both land-based and underwater waste categories.
* Deploy the best-performing model through a web-based interface.
* Support sustainable waste management and recycling initiatives.

---

## 🗂 Dataset

The project combines two publicly available datasets:

### 1. RealWaste Dataset

* Land-based waste images
* 9 waste categories:

  * Plastic
  * Paper
  * Glass
  * Metal
  * Organic
  * Textile
  * Cardboard
  * Vegetation
  * Miscellaneous

### 2. FIT Competition Final Round 2025 Dataset

* Underwater waste images
* 4 waste categories:

  * Plastic
  * Glass
  * Metal
  * Miscellaneous

### Dataset Statistics

* Total Images: ~5,600+
* Total Classes: 13
* Train : Validation : Test Split = 60 : 20 : 20

---

## 🔄 Data Preprocessing

* Image Resizing (224 × 224)
* Image Normalization
* Class Balancing
* Weighted Random Sampling
* Data Augmentation

### Augmentation Techniques

* Random Resized Crop
* Horizontal Flip
* Random Rotation
* Color Jitter
* Gaussian Blur
* RandAugment
* Random Erasing
* MixUp
* CutMix

---

## 🧠 Deep Learning Models Evaluated

The following CNN architectures were evaluated:

| Model         | Type            |
| ------------- | --------------- |
| ResNet-18     | Residual CNN    |
| ResNet-50     | Residual CNN    |
| MobileNetV2   | Lightweight CNN |
| MobileNetV3   | Lightweight CNN |
| DenseNet-121  | Dense CNN       |
| VGG-16        | Deep CNN        |
| VGG-19        | Deep CNN        |
| ConvNeXt      | Modern CNN      |
| ConvNeXt-Base | Modern CNN      |

---

## ✨ Attention Enhancement using CBAM

To improve feature discrimination, the Convolutional Block Attention Module (CBAM) was integrated into selected architectures.

### CBAM Components

* Channel Attention
* Spatial Attention

Benefits:

* Focuses on important image regions.
* Improves feature representation.
* Reduces misclassification of visually similar waste categories.

---

## 🏆 Best Model Performance

### ResNet-50 + CBAM

| Metric    | Value  |
| --------- | ------ |
| Accuracy  | 85.30% |
| Precision | 85.08% |
| Recall    | 85.38% |
| F1 Score  | 84.43% |

---

## 🌐 Web Application

The best-performing model is deployed through a Flask-based web interface.

### Features

* Upload waste images
* Real-time prediction
* Top-3 predicted classes
* Confidence score visualization
* Prediction latency display
* User feedback collection
* Admin dashboard
* Performance monitoring

---

## 🏗 Project Architecture

```text
Input Image
      │
      ▼
Data Preprocessing
      │
      ▼
CNN Backbone Models
      │
      ▼
CBAM Attention Module
      │
      ▼
Classification Layer
      │
      ▼
Prediction
      │
      ▼
Flask Web Application
```

---

## 🛠 Technologies Used

### Programming Language

* Python

### Deep Learning

* PyTorch
* TorchVision

### Data Processing

* NumPy
* Pandas

### Visualization

* Matplotlib
* Seaborn

### Web Development

* Flask
* HTML
* CSS
* JavaScript

### Database

* SQLite

