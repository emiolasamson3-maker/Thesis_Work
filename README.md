# 🧠 ADD-Net: Alzheimer’s Disease Detection from Structural MRI

> A deep learning framework for **automated Alzheimer’s disease classification and staging** using MRI, enhanced with attention mechanisms, imbalance handling, and explainable AI.

---

## 📌 Overview

This project introduces **ADD-Net Enhanced**, a custom convolutional neural network designed for **multi-class Alzheimer’s disease diagnosis** from structural MRI scans.

The framework delivers a **fully reproducible, end-to-end pipeline**, combining:
- Advanced preprocessing  
- Robust imbalance handling  
- Attention-based deep learning  
- Explainable AI techniques  

### 🎯 Classification Task
The model performs **4-class classification**:
- 🟢 NonDemented  
- 🟡 Very Mild Demented  
- 🟠 Mild Demented  
- 🔴 Moderate Demented  

---

## 🚀 Key Features

- 🧠 **ADD-Net + SE Attention**  
  Learns channel-wise importance to focus on clinically relevant features.

- ⚖️ **Severe Imbalance Handling**  
  Applies **SMOTETomek** to correct extreme class imbalance (~50:1).

- 🔄 **Optimised Training Strategy**
  - Cosine annealing with warm restarts  
  - Label smoothing  
  - Class-balanced weighting  

- 📊 **Comprehensive Evaluation**
  - Confusion matrix  
  - ROC curves  
  - Precision-Recall curves  
  - Per-class metrics  

- 🔍 **Explainable AI (XAI)**
  - Grad-CAM visualisations  
  - t-SNE feature embeddings  

- 📈 **Reproducibility First**
  Deterministic pipeline with fixed seeds.

---

## 🏗️ Pipeline Overview

```text
Environment Setup
   ↓
Configuration Management
   ↓
Dataset Loading & Label Mapping
   ↓
Class Imbalance Analysis
   ↓
Stratified Split (70/15/15)
   ↓
SMOTETomek Resampling (Train Only)
   ↓
Data Augmentation (tf.data)
   ↓
ADD-Net Model + SE Blocks
   ↓
Cosine LR Scheduling
   ↓
Model Training
   ↓
Evaluation (Test Set)
   ↓
Explainability (Grad-CAM, t-SNE)
   ↓
Model Saving & Reporting
