# 🗑️ Garbage Classification using EfficientNet

A deep learning project that classifies garbage images into **12 waste categories** using **EfficientNetB0** and transfer learning.

---

## 🚀 Overview
- Multi-class image classification problem
- Uses **EfficientNetB0 (ImageNet pretrained)**
- Focus on **high accuracy and generalization**
- Final model selected based on **test performance**

---

## 🧠 Classes (12)
battery, biological, brown-glass, cardboard, clothes,  
green-glass, metal, paper, plastic, shoes, trash, white-glass

---

## 📦 Dataset
- Source: **[Kaggle – Garbage Classification Dataset](https://www.kaggle.com/datasets/mostafaabla/garbage-classification)**
- Images organized in **class-wise folders**
- Split: **Train (80%) | Validation (10%) | Test (10%)**

---

## 🏗️ Model Architecture
- EfficientNetB0 backbone (`include_top=False`)
- Global Average Pooling
- Dropout (0.3)
- Dense Softmax output layer (12 classes)

---

## 🔁 Training Strategy
**Stage 1 – Transfer Learning**
- Backbone frozen
- Trained custom classification head
- Class weights + Early stopping
- Accuracy: 95.66%

**Stage 2 – Fine Tuning**
- Unfroze top convolution layers (last 40)
- Lower learning rate
- Accuracy: 92.53%

📌 **Final Model**: Stage-1 model (better test generalization)

---

## 📊 Results
- **Test Accuracy ≈ 95%+**
- Confusion Matrix & Classification Report used for evaluation

---

## 💾 Saved Artifacts
- `efficientnet_stage1_final.keras` – final trained model
- `class_names.json` – class label mapping

---

## 🛠️ Tech Stack
Python, TensorFlow/Keras, NumPy, Matplotlib, Scikit-learn, EfficientNet(base 0)

---

## 📌 Note
This project prioritizes **model performance and robustness**.  
Explainable AI (Grad-CAM) is explored separately on a cleaner architecture.

---
