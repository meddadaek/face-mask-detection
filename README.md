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
🧑‍💻 Author

Doro Kanji
💼 AI & Deep Learning Enthusiast
🐙 GitHub: meddadaek

⭐ Contribute

Contributions are welcome!
If you’d like to improve this project:

Fork the repository

Create a new branch (feature/new-feature)

Commit your changes

Push the branch and open a Pull Request

🏁 License

This project is open source under the MIT License.
Feel free to use, modify, and share it — but please give credit where due. 💙



⚡ "Deep Learning is not about coding — it’s about teaching machines how to see and understand."

##SOME OF THE OUTPUT

---<img width="403" height="598" alt="Screenshot 2025-11-03 165503" src="https://github.com/user-attachments/assets/dc64dac0-ed50-48fc-8ef5-eebf7bae577b" />
<img width="597" height="581" alt="Screenshot 2025-11-03 165557" src="https://github.com/user-attachments/assets/f0343a23-3709-44e9-87e3-cd9bb8c2ee27" />
