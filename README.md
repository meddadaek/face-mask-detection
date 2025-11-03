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

---

### 🧩 Visualization (Matplotlib)

Each prediction will show the image with a title containing the prediction and confidence percentage:

| Example 1 | Example 2 |
|:----------:|:----------:|
| ![Example 1](https://i.imgur.com/fZBzM8m.png) | ![Example 2](https://i.imgur.com/lnHxH1V.png) |
| 😷 **WITH MASK (98.45%)** | 😶 **WITHOUT MASK (97.83%)** |

*(These are sample images — replace them with your own results from your notebook or screenshots.)*

---

### 🧠 Model Behavior Summary

- ✅ Correctly predicts most clear frontal images.  
- ⚠️ Slightly less confident on angled faces or poor lighting.  
- 📈 Improves significantly with data augmentation and regularization.  

---

### 🎯 Example of Random Image Prediction Script

```python
import random, os
from tensorflow.keras.preprocessing import image
import numpy as np
import matplotlib.pyplot as plt

folders = [
    '/kaggle/input/face-mask-dataset/data/with_mask',
    '/kaggle/input/face-mask-dataset/data/without_mask'
]

folder = random.choice(folders)
img_file = random.choice(os.listdir(folder))
img_path = os.path.join(folder, img_file)

img = image.load_img(img_path, target_size=(128,128))
img_array = image.img_to_array(img) / 255.0
img_array = np.expand_dims(img_array, axis=0)

prediction = model.predict(img_array)
label = "😷 WITH MASK" if prediction[0][0] > 0.5 else "😶 WITHOUT MASK"
confidence = prediction[0][0]*100 if prediction[0][0]>0.5 else (1-prediction[0][0])*100

plt.imshow(image.load_img(img_path))
plt.title(f"{label} ({confidence:.2f}%)")
plt.axis('off')
plt.show()


⚡ "Deep Learning is not about coding — it’s about teaching machines how to see and understand."
