# Design and Evaluation of a CNN Architecture for Classifying Imbalanced Histopathological Images of Oral Cancer

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange)
![CNN](https://img.shields.io/badge/Model-CNN-green)
![Medical Imaging](https://img.shields.io/badge/Application-Oral%20Cancer-red)

## Overview

Oral Squamous Cell Carcinoma (OSCC) is one of the most common forms of oral cancer. Early diagnosis of OSCC plays a critical role in improving patient outcomes. Histopathological examination remains the gold standard for diagnosis, but manual analysis is time-consuming and subject to inter-observer variability.

This project presents a deep learning-based framework for automated classification of oral cancer histopathological images. A custom Convolutional Neural Network (CNN) architecture was designed and evaluated on multiple versions of an imbalanced oral cancer dataset. The proposed model was compared with several state-of-the-art pre-trained CNN architectures including VGG16, VGG19, DenseNet, MobileNet, Xception, EfficientNet, and InceptionV3.

The study investigates the impact of image preprocessing, data augmentation, and SMOTE-based balancing techniques on classification performance.

---

## Project Information

**Project Title:**
Design and Evaluation of a CNN Architecture for Classifying Imbalanced Histopathological Images of Oral Cancer

**Author:** Pragyan Chetia

**Degree:** Bachelor of Computer Application (BCA)

**Institution:** Centre for Computer Science and Applications, Dibrugarh University

**Supervisor:** Dr. Pranjal Kumar Bora

**Academic Session:** 2024–2025

---

## Objectives

* Develop a custom CNN model for oral cancer classification.
* Compare the proposed model with established deep learning architectures.
* Investigate the effect of dataset balancing strategies.
* Improve classification performance through image preprocessing and augmentation.
* Identify the most effective dataset preparation strategy for OSCC classification.

---

## Dataset

The study uses the Histopathological Imaging Database for Oral Cancer Analysis.

### Dataset Characteristics

| Category      | Samples |
| ------------- | ------- |
| Normal Tissue | 201     |
| OSCC Tissue   | 495     |
| Total Images  | 696     |

### Image Specifications

* H&E stained biopsy images
* Magnification: 400×
* Resolution: 2048 × 1536 pixels
* Binary Classification:

  * Normal
  * Oral Squamous Cell Carcinoma (OSCC)

---

## Dataset Variants

Three datasets were prepared and evaluated:

### 1. Original Dataset

* Preprocessed images
* Retains original class imbalance

### 2. Augmented Dataset

* Rotation
* Flipping
* Zooming
* Shifting

Both classes expanded to approximately 5000 images.

### 3. SMOTE + Augmented Dataset

* SMOTE applied to minority class
* Followed by image augmentation
* Produces a balanced and diversified dataset

---

## Image Preprocessing Pipeline

The following preprocessing steps were applied:

1. Image Resizing (256 × 256)
2. Median Filtering for noise removal
3. CLAHE (Contrast Limited Adaptive Histogram Equalization)
4. Normalization

These steps improve tissue visibility, enhance contrast, and reduce staining artifacts.

---

## Proposed CNN Architecture

The proposed CNN consists of:

* 8 Convolution Layers
* 5 MaxPooling Layers
* 2 Dropout Layers
* Flatten Layer
* 3 Dense Layers
* Softmax Output Layer

Architecture Flow:

Input Image
→ Conv Layers
→ MaxPooling
→ Dropout
→ Flatten
→ Fully Connected Layers
→ Softmax Classification

Total Parameters: 768,642

---

## Models Evaluated

The proposed CNN was compared against:

* VGG16
* VGG19
* DenseNet
* MobileNet
* Xception
* EfficientNet
* InceptionV3

---

## Performance Metrics

The following evaluation metrics were used:

* Accuracy
* Precision
* Recall
* F1 Score
* AUC Score
* Confusion Matrix
* ROC Curve

---

## Results

The proposed CNN achieved the best overall performance.

### Best Performance

| Dataset           | Accuracy |
| ----------------- | -------- |
| Augmented Dataset | 99.16%   |

Additional metrics on the augmented dataset:

* F1 Score: 88.39
* AUC Score: 89.08

The proposed CNN outperformed all evaluated pre-trained architectures.

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Pandas
* Scikit-Learn
* OpenCV
* Matplotlib
* Google Colab
* Jupyter Notebook

---

## Repository Structure

```text
project/
│
├── dataset/
├── preprocessing/
├── augmentation/
├── models/
├── notebooks/
├── results/
├── figures/
├── README.md
└── requirements.txt
```

---

## Key Contributions

* Designed a custom CNN architecture specifically for oral cancer histopathology.
* Evaluated multiple balancing strategies for imbalanced medical datasets.
* Demonstrated the effectiveness of CLAHE-based preprocessing.
* Achieved 99.16% classification accuracy on the augmented dataset.
* Provided comparative analysis against multiple transfer learning architectures.

---

## Future Work

* Integration of explainable AI techniques (Grad-CAM, SHAP).
* Multi-class oral lesion classification.
* Whole-slide image analysis.
* Clinical deployment and validation on larger datasets.
* Integration with computer-aided diagnostic systems.

---

## Citation

```bibtex
@thesis{chetia2025oralcancer,
  title={Design and Evaluation of a CNN Architecture for Classifying Imbalanced Histopathological Images of Oral Cancer},
  author={Pragyan Chetia},
  school={Dibrugarh University},
  year={2025},
  type={Bachelor's Thesis}
}
```

## Disclaimer

This project was developed for academic and research purposes. The model is not intended for clinical diagnosis without further validation and regulatory approval.
