# 🧠 Intelligent Deep Learning Framework for Alzheimer’s Disease Detection & Staging

## 🚀 Overview

This project presents an advanced deep learning framework for the **automated detection and multi-class staging of Alzheimer’s disease (AD)** using structural MRI data.

The proposed system, **ADD-Net Enhanced**, integrates attention-driven convolutional architectures with robust imbalance handling and explainable AI techniques to deliver **accurate, interpretable, and clinically relevant predictions**.

---

## 🎯 Objectives

* Detect Alzheimer’s disease across multiple stages using MRI scans  
* Improve classification performance under **severe class imbalance**  
* Enhance model interpretability for clinical trust and transparency  
* Develop a robust and reproducible end-to-end deep learning pipeline  
* Provide a scalable framework for AI-driven neuroimaging analysis  

---

## 🗂️ Dataset

**Structural MRI Alzheimer’s Dataset**

* Multi-class neuroimaging dataset  
* Four diagnostic categories:
  - NonDemented  
  - Very Mild Demented  
  - Mild Demented  
  - Moderate Demented  

> ⚠️ The dataset exhibits **extreme class imbalance (~50:1)**, which is explicitly addressed in this study.

---

## 🧠 Methodology

### 🔹 1. Data Processing

* MRI preprocessing and standardisation  
* Label encoding and dataset structuring  
* Efficient pipeline using `tf.data`  

---

### 🔹 2. Handling Class Imbalance

* **SMOTETomek (Hybrid Resampling Technique)**  
  - SMOTE → generates synthetic minority samples  
  - Tomek Links → removes noisy majority samples  

> ⚠️ Applied **only to the training set** to preserve real-world evaluation.

---

### 🔹 3. Model Architecture

#### 🧩 Deep Learning Model

* **ADD-Net Enhanced (CNN + SE Attention)**  

  * Convolutional feature extraction  
  * Batch Normalisation & Dropout  
  * **Squeeze-and-Excitation (SE) Blocks** for channel attention  
  * Focuses on clinically relevant brain structures  

---

### 🔹 4. Training Strategy

* **Cosine Annealing with Warm Restarts**  
* Label smoothing for regularisation  
* Class-balanced learning  
* Early stopping and checkpointing  

---

### 🔹 5. Explainable AI

* **Grad-CAM**

  * Highlights brain regions influencing predictions  

* **t-SNE Feature Visualisation**

  * Reveals class separability in learned representations  

---

## 📊 Evaluation Metrics

Model performance is assessed using:

* Accuracy  
* Precision  
* Recall  
* F1 Score  
* ROC-AUC (multi-class)  
* Confusion Matrix  
* Precision-Recall Curves  

---

## 📈 Key Contributions

* Novel **ADD-Net architecture with attention mechanisms**  
* Robust handling of **extreme class imbalance**  
* Integration of **Explainable AI for medical imaging**  
* End-to-end reproducible deep learning pipeline  
* Clinically relevant multi-class Alzheimer’s staging approach  

---

## ⚙️ Tech Stack

* Python 🐍  
* TensorFlow / Keras  
* Scikit-learn  
* Imbalanced-learn  
* NumPy & Pandas  
* Plotly (visualisation)  

---
▶️ How to Run
Clone the repository:
git clone https://github.com/username/code.git
Install dependencies:
pip install tensorflow scikit-learn imbalanced-learn pandas plotly scipy
Launch the notebook:
jupyter notebook code.ipynb

---

🔮 Future Work
Integration of 3D CNN architectures for volumetric MRI
Transformer-based medical imaging models
Longitudinal disease progression modelling
Deployment as a clinical decision support system
External validation on diverse datasets

---

⚠️ Disclaimer

This project is for research and educational purposes only and is not intended for direct clinical application without further validation.

---

👤 Author
Emiola Samson
MSc Data Science Project
Deep Learning · Medical Imaging · Explainable AI

---

🌟 Acknowledgements
Research community in medical imaging and AI
Open-source contributors in deep learning frameworks



