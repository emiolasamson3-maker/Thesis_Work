🧠 ADD-Net: Alzheimer’s Disease Detection from Structural MRI

A deep learning framework for automated Alzheimer’s disease staging using structural MRI, enhanced with attention mechanisms, advanced imbalance handling, and explainable AI.

📌 Overview

This project presents an end-to-end, reproducible pipeline for multi-class Alzheimer’s disease classification. It introduces ADD-Net Enhanced, a custom CNN architecture integrated with Squeeze-and-Excitation (SE) attention to improve feature discrimination in MRI scans.

The system performs 4-class classification:

NonDemented
Very Mild Demented
Mild Demented
Moderate Demented
🚀 Key Features
🧠 Custom Architecture (ADD-Net + SE Attention)
Learns channel-wise feature importance for improved diagnostic focus.
⚖️ Advanced Class Imbalance Handling
Uses SMOTETomek to address extreme imbalance (~50:1 ratio).
🔄 Robust Training Strategy
Cosine annealing with warm restarts
Label smoothing
Class-balanced weighting
📊 Comprehensive Evaluation Suite
Confusion matrix
ROC & Precision-Recall curves
Per-class metrics
🔍 Explainable AI (XAI)
Grad-CAM visualisations
t-SNE feature space embeddings
📈 Reproducible Pipeline
Fully deterministic with fixed seeds across all libraries.
🏗️ Project Pipeline

The workflow follows a structured deep learning pipeline:

Environment Setup & Reproducibility
Centralised Configuration Management
Dataset Discovery & Label Mapping
Class Imbalance Analysis
Stratified Train/Validation/Test Split (70/15/15)
SMOTETomek Resampling (Training Set Only)
Data Augmentation via tf.data Pipeline
ADD-Net Model Construction with SE Blocks
Cosine Learning Rate Scheduling
Model Training with Callbacks
Evaluation on Unseen Test Set
Interpretability (Grad-CAM & t-SNE)
Model Saving & Final Reporting
🧪 Methodology Highlights
🔹 Class Imbalance Strategy

The dataset exhibits severe imbalance, where minority classes are underrepresented.

To address this:

SMOTE generates synthetic minority samples
Tomek Links remove noisy majority samples

⚠️ Resampling is applied only to the training set to preserve real-world distribution in evaluation.

🔹 Model Architecture

ADD-Net Enhanced integrates:

Convolutional feature extraction
Batch normalisation & dropout
Squeeze-and-Excitation (SE) blocks for channel attention

This allows the network to focus on clinically relevant brain regions.

🔹 Training Strategy
Optimiser: Adaptive (e.g., Adam)
Learning Rate: Cosine Annealing with Warm Restarts
Regularisation:
Label smoothing
Early stopping
Checkpointing
🔹 Explainability

To ensure clinical relevance:

Grad-CAM highlights important MRI regions influencing predictions
t-SNE visualises learned feature separability
📊 Evaluation Metrics

Model performance is assessed using:

Accuracy
Precision, Recall, F1-score
ROC-AUC (per class + macro/micro)
Confusion Matrix
Precision-Recall Curves

All evaluation is performed on a hold-out test set with original class distribution.

🛠️ Tech Stack
Python
TensorFlow / Keras
scikit-learn
imbalanced-learn
NumPy / Pandas
Plotly (visualisation)
SHAP / Grad-CAM (interpretability)
📂 Project Structure
├── code.ipynb              # Main notebook (full pipeline)
├── dataset/                # MRI dataset (not included)
├── checkpoints/            # Saved model weights
├── README.md               # Project documentation
⚙️ Installation
pip install tensorflow scikit-learn imbalanced-learn plotly pandas scipy
▶️ Usage
Clone the repository:
git clone https://github.com/lrrmrrrk-tech/final-code.git
cd final-code
Open the notebook:
jupyter notebook code.ipynb
Update dataset path in the configuration section:
WORKING_DIRECTORY = './dataset/'
Run all cells sequentially.
💾 Model Output
Trained model saved in .keras format
Evaluation reports and visualisations generated within notebook
⚠️ Notes
Requires high memory (~2GB+) for SMOTETomek processing
GPU recommended for training
Dataset not included due to size/usage restrictions
🎯 Contribution

This project contributes:

A robust framework for Alzheimer’s staging
A balanced learning strategy for extreme class imbalance
Integration of explainable AI in medical imaging
📜 License

This project is for academic and research purposes only.

👤 Author

MSc Data Science Project
Deep Learning · Medical Imaging · Explainable AI
