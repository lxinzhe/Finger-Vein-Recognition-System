# Finger-Vein-Recognition-System
A finger vein recognition system based on texture analysis. It utilizes Watershed Segmentation for ROI extraction, Histogram Equalization for image enhancement, and Local Binary Pattern (LBP) for feature extraction, evaluated on the UTFVP dataset.
# Finger Vein Recognition System Based on Texture Analysis

## 📖 Overview
Finger Vein Recognition is an emerging biometric modality valued for its high security and anti-spoofing characteristics, as it utilizes the internal vascular structure hidden beneath the skin[cite: 3]. This repository contains an offline software prototype that processes near-infrared (NIR) finger vein images to perform biometric identity verification[cite: 3]. 

## ⚙️ Methodology & Pipeline
The system architecture follows a four-phase operational flow:
* **Image Preprocessing:** Uses Watershed Segmentation to localize the Region of Interest (ROI) and separates the finger tissue from background noise[cite: 3].
* **Image Enhancement:** Applies Histogram Equalization to redistribute pixel intensity and increase the contrast of subcutaneous vascular patterns[cite: 3].
* **ROI Normalization:** Resizes the extracted finger vein region to a fixed resolution of 120x320 pixels to ensure scale invariance across the dataset[cite: 3].
* **Texture Feature Extraction:** Utilizes a Uniform Local Binary Pattern (LBP) operator (P=8, R=1) to capture micro-textures and vein bifurcations, generating a high-dimensional feature vector[cite: 3].
* **Classification & Matching:** Employs a One-vs-Rest Logistic Regression machine learning model for identity verification[cite: 3].

## 📊 Dataset
The system is evaluated using the **University of Twente Finger Vein Pattern (UTFVP) database**[cite: 3]. The experimental analysis in this repository specifically focuses on the Left Index (LI) finger subset to benchmark the feature extraction algorithm[cite: 3].

## 💻 Tech Stack & Requirements
* **Language:** Python 3.10+[cite: 3]
* **Environment:** Anaconda, Jupyter Notebook / Visual Studio Code[cite: 3]
* **Core Libraries:** 
  * `NumPy` & `Pandas` for data processing and matrix operations[cite: 3].
  * `scikit-image` for Watershed segmentation, Histogram Equalization, and LBP extraction[cite: 3].
  * `scikit-learn` for Logistic Regression classification and Equal Error Rate (EER) computation[cite: 3].

## 📈 Results
The current implementation serves as a functional baseline for automated biometric verification[cite: 3]. 
* **Identification Accuracy:** 61.11%[cite: 3]
* **Equal Error Rate (EER):** 38.89%[cite: 3]

## 🚀 Future Enhancements
Future iterations of this project (FYP 2) will focus on:
* Replacing the linear Logistic Regression model with non-linear classifiers like Support Vector Machines (SVM) and Random Forests to better handle complex high-dimensional features[cite: 3].
* Implementing Multi-scale LBP (variable radii and neighbor counts) to capture larger vein structures[cite: 3].
