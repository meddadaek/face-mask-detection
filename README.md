# 😷 Face Mask Detection using CNN (TensorFlow & Keras)

A deep learning project that detects whether a person **is wearing a face mask or not** using a **Convolutional Neural Network (CNN)**.  
Built with **TensorFlow/Keras**, this project demonstrates end-to-end image classification — from data preprocessing to model training and prediction.

---

## 🧠 Project Overview

During the COVID-19 pandemic, face mask detection became an essential computer vision application.  
This project aims to automatically classify facial images into two categories:

- 😷 **With Mask**
- 😶 **Without Mask**

Using Convolutional Neural Networks (CNNs), the model learns to identify subtle differences in facial features between masked and unmasked faces.  
The trained model can later be integrated into real-time systems such as webcam apps or surveillance tools.

---

## 📂 Dataset

The dataset used in this project is the **Face Mask Dataset** (available on Kaggle or other public sources).

### Structure:
data/
│
├── with_mask/
│ ├── with_mask_1.jpg
│ ├── with_mask_2.jpg
│ └── ...
│
└── without_mask/
├── without_mask_1.jpg
├── without_mask_2.jpg
└── ...


- **With Mask:** 3725 images  
- **Without Mask:** 3828 images  
- **Total:** 7553 images

All images were resized, normalized, and split into training and validation sets during preprocessing.

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/meddadaek/face-mask-detection.git
cd face-mask-detection

2️⃣ Install dependencies
pip install -r requirements.txt
