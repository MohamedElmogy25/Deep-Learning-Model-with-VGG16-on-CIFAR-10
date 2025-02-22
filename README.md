# 🌿 Plant Disease Classification using VGG16

## 📌 Overview
This project utilizes a pre-trained **VGG16** model for **plant disease classification**. The dataset used is **PlantVillage**, which contains images of tomato leaves affected by various diseases. The model is fine-tuned to recognize **9 different classes** of tomato leaf diseases.

## 📂 Dataset
The dataset consists of **14,335 images** across **9 classes**, split into:
- **Training Set:** 11,468 images (80%)
- **Validation Set:** 2,867 images (20%)

### 🏷 Classes:
1. 🍅 Tomato_Bacterial_spot
2. 🍅 Tomato_Early_blight
3. 🍅 Tomato_Late_blight
4. 🍅 Tomato_Leaf_Mold
5. 🍅 Tomato_Septoria_leaf_spot
6. 🍅 Tomato_Target_Spot
7. 🍅 Tomato_Tomato_YellowLeaf_Curl_Virus
8. 🍅 Tomato_Tomato_mosaic_virus
9. ✅ Tomato_healthy

## 🏗 Model Architecture
The model is based on **VGG16**, a deep convolutional neural network. The pre-trained base model is used without its top layers, and custom **fully connected layers** are added for classification:

1. **VGG16 Base Model** (Pre-trained on ImageNet, frozen layers)
2. **Flatten Layer**
3. **Dense Layer (512 neurons, ReLU activation)**
4. **Dropout (0.5)**
5. **Dense Layer (256 neurons, ReLU activation)**
6. **Dropout (0.3)**
7. **Output Layer (9 neurons, Softmax activation)**

## ⚙ Installation
### Prerequisites
Ensure you have Python and the required libraries installed:
```sh
pip install tensorflow matplotlib numpy seaborn
```

## 🚀 Usage
### 1️⃣ Train the Model

### 2️⃣ Fine-Tune the Model
After initial training, the last 4 layers of VGG16 are unfrozen for fine-tuning.

### 3️⃣ Evaluate the Model
## 📊 Results
### 📈 Training Performance
The model is trained for **10 epochs**, followed by **5 fine-tuning epochs**. Accuracy and loss plots are generated automatically.

### 🔍 Visualizations
1. **Training Accuracy & Loss Graphs** 📉
2. **Sample Predictions on Validation Set** 🖼
3. **Confusion Matrix** 🏆

## 💾 Model Saving
The trained model is saved as `plant_disease_model.h5` for future inference.

## ✨ Contributors
- **Mohamed Elmogy** 👨‍💻

## 📜 License
This project is open-source and available under the **MIT License**.

## 📚 References
- [PlantVillage Dataset](https://www.kaggle.com/datasets/emmarex/plantdisease)
- [VGG16 Paper](https://arxiv.org/abs/1409.1556)

---
🔹 *Feel free to contribute and improve this project!* 🚀
