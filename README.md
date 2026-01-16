# 🧠 Convolutional Neural Network using PyTorch
This is my step into image segmentation and convolution neural networks, and a try to understand convolution layers, maxpool and overall image classification. I have applied this model on CIFAR 10 dataset

## 📌 Project Overview

This project is my **first Convolutional Neural Network (CNN)** focused on **image classification** 🖼️.  
It serves as a **proof of concept** for understanding how **convolutional layers extract spatial features** and how these features transition into **linear classification**.

The model was trained on the **CIFAR-10 dataset** to explore the complete CNN workflow — from feature extraction to final prediction 🚀.

---

## 📂 Dataset

**CIFAR-10**  
- A widely used dataset for computer vision tasks  
- 🖼️ **Data Type:** Color images (RGB)  
- 🏷️ **Classes:** 10 (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)  
- 📐 **Image Size:** \(32 \times 32\) pixels  
- 🎨 **Channels:** 3 (RGB)

---

## 🛠️ Tools & Technologies

- 🔥 **PyTorch** – Core framework for CNN architecture and training  
- 🧰 **Torchvision** – Dataset loading and data augmentation  
- 🐍 **Python** – Programming language  

---

## 🚧 Progress Involved

### 1️⃣ Loading the Data
- Imported the CIFAR-10 dataset
- Applied transformations using `transforms.Compose`:
  - `ToTensor()` to convert images into tensors
  - `Normalize()` to standardize RGB channels
- Split the dataset into:
  - 🏋️ `trainloader`
  - 🧪 `testloader`

---

### 2️⃣ Building the Model

#### 🔹 Convolutional Feature Extractor
- Used `nn.Conv2d` layers to extract spatial features
- Learned local patterns such as edges and textures

#### 🔹 Activation & Pooling
- Applied **ReLU** ⚡ for non-linearity
- Used `MaxPool2d` to:
  - Reduce spatial dimensions
  - Control overfitting
  - Improve computational efficiency

#### 🔹 Classifier
- Flattened multi-dimensional feature maps into a 1D vector
- Used `nn.Linear` layers to map features to **10 output classes**

#### 🔹 Forward Function
```Conv → ReLU → Pool → Flatten → Fully Connected
