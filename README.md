# 🗑️ Garbage Classification using EfficientNet

*A deep learning project for classifying garbage images into **12 waste categories** using **EfficientNetB0** and transfer learning.*

---

## 🚀 Overview
- **Multi-class image classification**
- **EfficientNetB0 (ImageNet pretrained)**
- Focus on **high accuracy & strong generalization**
- **Best model selected based on test performance**

---

## 🧠 Classes (12)
`battery`, `biological`, `brown-glass`, `cardboard`, `clothes`,  
`green-glass`, `metal`, `paper`, `plastic`, `shoes`, `trash`, `white-glass`

---

## 📦 Dataset
- **Source:** [Kaggle – Garbage Classification Dataset](https://www.kaggle.com/datasets/mostafaabla/garbage-classification)
- Images organized in **class-wise folders**
- **Data Split:**  
  - 🟢 Train — 80%  
  - 🟡 Validation — 10%  
  - 🔵 Test — 10%

---

## 🏗️ Model Architecture
- **EfficientNetB0** backbone (`include_top=False`)
- **Global Average Pooling**
- **Dropout (0.3)** for regularization
- **Dense Softmax layer** (12 classes)

---

## 🔁 Training Strategy

### 🔹 Stage 1 – Transfer Learning
- Backbone **frozen**
- Trained **custom classification head**
- **Class weights** + **Early stopping**
- **Accuracy:** **95.66%**

### 🔹 Stage 2 – Fine Tuning
- Unfroze **top convolution layers (last 40)**
- **Lower learning rate**
- **Accuracy:** **92.53%**

📌 **Final Model Chosen:**  
👉 *Stage-1 model (better generalization on test data)*

---

## 📊 Results
- **Test Accuracy:** **≈ 95%+**
- Evaluation using:
  - Confusion Matrix  
  - Classification Report (Precision, Recall, F1-score)

---

## 💾 Saved Artifacts
- `efficientnet_stage1_final.keras` → **final trained model**
- `class_names.json` → **class label mapping**

---

## 🛠️ Tech Stack
**Python**, **TensorFlow/Keras**, **EfficientNetB0**,  
NumPy, Matplotlib, Scikit-learn

---

## 📌 Note
This project prioritizes **model performance and robustness**.  
**Explainable AI (Grad-CAM)** is explored separately on a cleaner architecture.

---
