# 🌿 Leaf Classification Model (CNN)

## 📌 Project Overview

This project is an image classification system developed to identify different types of tree leaves using deep learning. The model is built using Convolutional Neural Networks (CNN) and trained on a dataset containing 12 leaf classes.

---

## 📥 Model Download

### 🔹 Implementation 1 (Baseline Model)

👉 https://drive.google.com/file/d/19A-aPKsMkWgzhn_sWNg684GlsqMevrH8/view?usp=drive_link

### 🔹 Implementation 2 (Improved Model)

👉 https://drive.google.com/file/d/1r6V7HMrBK1Wkb71Qu7vNcBt3TAu4o6y3/view?usp=drive_link

---

## 🧠 Model Details

* Model Type: Convolutional Neural Network (CNN)
* Number of Classes: 12
* Image Size: 128 × 128
* Framework: TensorFlow / Keras

---

## ⚙️ How to Use the Model

### 1️⃣ Install Required Libraries

```bash id="z2f3x0"
pip install tensorflow numpy matplotlib
```

### 2️⃣ Load the Model

```python id="ksn5uv"
from tensorflow.keras.models import load_model

model = load_model("model_name.h5")   # Replace with downloaded model name
```

### 3️⃣ Prepare an Image

```python id="j2qpj2"
from tensorflow.keras.preprocessing import image
import numpy as np

img = image.load_img("leaf.jpg", target_size=(128,128))
img_array = image.img_to_array(img)
img_array = np.expand_dims(img_array, axis=0) / 255.0
```

### 4️⃣ Make Prediction

```python id="xljk7k"
prediction = model.predict(img_array)
predicted_class = np.argmax(prediction)

print("Predicted Class:", predicted_class)
```

---

## 📁 Dataset Structure

```id="f0wxt9"
leaves/
   train/
   test/
```

Each folder contains 12 leaf categories.

---

## 🚀 Improvements in Implementation 2

* Data augmentation (rotation, zoom, flipping)
* Deeper CNN architecture
* Dropout regularization
* Early stopping to reduce overfitting

---

## ⚠️ Notes

* Implementation 1 is a baseline model.
* Implementation 2 improves generalization and reduces overfitting.

---

## 👨‍💻 Project Type

Mini Project – Image Classification (Leaf Recognition System)

---





