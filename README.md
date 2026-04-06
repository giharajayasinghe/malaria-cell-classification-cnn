Malaria Cell Classification using CNN vs DNN

## 📌 Overview
This project focuses on classifying malaria-infected blood smear images using deep learning.  
A comparison is made between a Dense Neural Network (DNN) and a Convolutional Neural Network (CNN) to highlight their performance differences in image classification tasks.

---

## 📂 Dataset
- Source: NIH Malaria Dataset  
- Link: https://data.lhncbc.nlm.nih.gov/public/Malaria/cell_images.zip  
- Classes:
  - Parasitized (infected)
  - Uninfected

---

## ⚙️ Preprocessing
- Resized all images to **28×28**
- Converted images to tensors
- Binary label transformation (0/1)

---

## 🧠 Models Implemented

### 🔹 Dense Neural Network (DNN)
- Input: Flattened image (28×28×3)
- Architecture: 2 hidden layers (128 neurons each)
- Activation: Sigmoid
- Parameters: ~317K

### 🔹 Convolutional Neural Network (CNN)
- Convolutional layers with pooling
- Adaptive average pooling
- Fully connected output layer
- Parameters: ~16.7K

---

## 📊 Results

| Model | Accuracy | Parameters | ROC AUC |
|------|--------|-----------|--------|
| DNN  | ~68%   | 317K      | Lower |
| CNN  | ~94%   | 16.7K     | 0.985 |

### 📈 Key Insight
The CNN significantly outperformed the DNN while using far fewer parameters.  
This demonstrates the importance of spatial feature extraction in image classification tasks.

---

## 📉 ROC Curves

### DNN
![DNN ROC](dnn_roc.png)

### CNN
![CNN ROC](cnn_roc.png)

---

## 🛠️ Tech Stack
- Python
- PyTorch
- Deeplay
- TorchMetrics
- Matplotlib

---

## ▶️ How to Run

```bash
pip install torch torchvision deeplay torchmetrics matplotlib
