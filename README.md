# 🧠 Handwritten Digit Recognition using MLP (MNIST)

## 📌 Project Overview
This project implements a **Multilayer Perceptron (MLP)** neural network for handwritten digit classification using the **MNIST dataset**.

The goal is to analyze the impact of different hyperparameters—such as activation functions and hidden layer sizes—on model performance.

Two experiments were conducted for comparison:
- Experiment 1: ReLU activation with 128 hidden neurons
- Experiment 2: Sigmoid activation with 256 hidden neurons

---

## 📊 Dataset

- Dataset: MNIST Handwritten Digits
- Source: PyTorch torchvision
- Official Link: [http://yann.lecun.com/exdb/mnist/](https://docs.pytorch.org/vision/stable/datasets.html)
- Number of classes: 10 (digits 0–9)
- Image size: 28 × 28 grayscale

### 🔧 Preprocessing
- Convert images to tensors
- Normalize images (mean = 0.5, std = 0.5)
- Standard train/test split provided by MNIST dataset

---

## 🧠 Model Architecture

A simple **MLP (Multilayer Perceptron)** is used:

- Input Layer: 784 neurons (flattened 28×28 image)
- Hidden Layer: 128 or 256 neurons (based on experiment)
- Output Layer: 10 neurons (classification output)

### 🔥 Activation Functions Used
- ReLU (Experiment 1)
- Sigmoid (Experiment 2)

---

## ⚙️ Training Configuration

- Loss Function: CrossEntropyLoss
- Optimizer: Adam
- Learning Rate: 0.001
- Batch Size: 64
- Epochs: 10
- Device: GPU (if available) / CPU fallback

---

## 📏 Evaluation Metrics

The model is evaluated using:

- Accuracy (primary metric for classification)
- Training Loss
- Testing Loss
- Final Test Accuracy

---

## 🧪 Experiments

### 🔹 Experiment 1
- Activation Function: ReLU  
- Hidden Neurons: 128  

### 🔹 Experiment 2
- Activation Function: Sigmoid  
- Hidden Neurons: 256  

---

## 📈 Results

| Experiment   | Activation | Hidden Units | Final Test Accuracy |
|-------------|------------|--------------|---------------------|
| ReLU_128    | ReLU       | 128          | 96.88%              |
| Sigmoid_256 | Sigmoid    | 256          | 97.86%              |

---

## 🔍 Observations

- Both models achieved strong performance (>96% accuracy).
- Increasing hidden layer size improved performance slightly.
- Sigmoid with higher capacity slightly outperformed ReLU in this setup.
- MLP performs well for MNIST, but CNN models are generally more powerful for image classification.

---

## 📊 Visualizations

The following visualizations are included in the project:

- Training vs Testing Loss curves
- Accuracy comparison between experiments

---

## 🚀 How to Run

pip install -r requirements.txt

---

### Future Improvements
```bash
Add Dropout for regularization
Add Batch Normalization
Try deeper MLP architecture
Compare with CNN model for better accuracy
