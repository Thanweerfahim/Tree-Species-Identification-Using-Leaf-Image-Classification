# 🌿 Leaf Classification Model (Implementation 1)

## 📌 Project Overview

This project is an image classification system developed to identify different types of tree leaves using deep learning. The model is built using a Convolutional Neural Network (CNN) and trained on a dataset containing multiple leaf classes.

---

## 📥 Model Download

You can download the trained Implementation 1 model from the link below:

👉 (https://drive.google.com/file/d/19A-aPKsMkWgzhn_sWNg684GlsqMevrH8/view?usp=drive_link)

---

## 🧠 Model Details

* Model Type: Convolutional Neural Network (CNN)
* Number of Classes: 12
* Image Size: 128 × 128
* Framework: TensorFlow / Keras
* File Format: `.keras`

---

## 📊 Performance

* Training Accuracy: ~91%
* Validation Accuracy: ~82%
* Test Accuracy: ~82%

---

## ⚙️ How to Use the Model

### 1️⃣ Install Required Libraries

```bash
pip install tensorflow numpy matplotlib
```

### 2️⃣ Load the Model

```python
from tensorflow.keras.models import load_model

model = load_model("binary_cnn_model.keras")
```

### 3️⃣ Prepare an Image

```python
from tensorflow.keras.preprocessing import image
import numpy as np

img = image.load_img("leaf.jpg", target_size=(128,128))
img_array = image.img_to_array(img)
img_array = np.expand_dims(img_array, axis=0) / 255.0
```

### 4️⃣ Make Prediction

```python
prediction = model.predict(img_array)
predicted_class = np.argmax(prediction)

print("Predicted Class:", predicted_class)
```

---

## 📁 Dataset Structure

```
leaves/
   train/
   test/
```

Each folder contains 12 leaf categories.

---

## ⚠️ Notes

* This is the **baseline model (Implementation 1)**.
* The model shows slight overfitting and can be improved using data augmentation and tuning (Implementation 2).

---

## 👨‍💻 Developed For

Mini Project – Image Classification (Leaf Recognition System)

---
