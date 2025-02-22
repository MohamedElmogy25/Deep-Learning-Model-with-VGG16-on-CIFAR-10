# Plant-Disease-Classification-using-VGG16
Plant Disease Classification using VGG16

Overview

This project uses a pre-trained VGG16 model to classify plant diseases from images. The dataset used is PlantVillage, which contains images of tomato leaves affected by various diseases. The model is fine-tuned to recognize 9 different classes of tomato leaf diseases.

Dataset

The dataset consists of 14,335 images across 9 classes, split into:

Training Set: 11,468 images (80%)

Validation Set: 2,867 images (20%)

Classes:

Tomato_Bacterial_spot

Tomato_Early_blight

Tomato_Late_blight

Tomato_Leaf_Mold

Tomato_Septoria_leaf_spot

Tomato_Target_Spot

Tomato_Tomato_YellowLeaf_Curl_Virus

Tomato_Tomato_mosaic_virus

Tomato_healthy

Model Architecture

The model is based on VGG16, a deep convolutional neural network. The pre-trained base model is used without its top layers, and custom fully connected layers are added for classification:

VGG16 Base Model (Pre-trained on ImageNet, frozen layers)

Flatten Layer

Dense Layer (512 neurons, ReLU activation)

Dropout (0.5)

Dense Layer (256 neurons, ReLU activation)

Dropout (0.3)

Output Layer (9 neurons, Softmax activation)

Installation

Prerequisites

Ensure you have Python and the required libraries installed:

pip install tensorflow matplotlib numpy seaborn

Usage

1. Train the Model

Run the following command to train the model:

python train.py

2. Fine-Tune the Model

After initial training, the last 4 layers of VGG16 are unfrozen for fine-tuning.

3. Evaluate the Model

To test the model on the validation dataset:

python evaluate.py

Results

Training Performance

The model is trained for 10 epochs, followed by 5 fine-tuning epochs. Accuracy and loss plots are generated automatically.

Visualizations

Training Accuracy & Loss Graphs

Sample Predictions on Validation Set

Confusion Matrix

Model Saving

The trained model is saved as plant_disease_model.h5 for future inference.

Contributors

[Your Name]

License

This project is open-source and available under the MIT License.

References

PlantVillage Dataset

VGG16 Paper

