# Detecting Deepfake Images

## Overview

This project detects **deepfake images using deep learning**.
The system uses a **ResNet18 convolutional neural network with transfer learning** to classify images as **Real or Fake**.

The project demonstrates an **end-to-end AI application pipeline** including:

* Model training
* Dataset preprocessing
* Deep learning inference
* REST API deployment
* Web interface for prediction

---

## Tech Stack

Python
PyTorch
ResNet18 (Transfer Learning)
Flask
HTML + TailwindCSS
NumPy
Pillow

---

## Model Architecture

The model uses **ResNet18 pretrained on ImageNet**.

Steps:

1. Input image resized to **224×224**
2. Image converted to tensor
3. Features extracted using **ResNet18 CNN layers**
4. Final fully connected layer modified for **binary classification**
5. Output classes:

   * Fake
   * Real

Loss Function:

CrossEntropyLoss

Optimizer:

Adam Optimizer (learning rate = 0.0001)

---

## Dataset Structure

dataset/

train/
 fake/
 real/

valid/
 fake/
 real/

Images are stored according to their class labels.

---

## Training

Run the training script:

```bash
python train_model.py
```

Example training output:

Epoch 1/10 | Train Acc: 76.2% | Val Acc: 72.4%
Epoch 5/10 | Train Acc: 88.3% | Val Acc: 84.7%

## Application Demo

### Real Image Detection

![Real Prediction](real_prediction.png)

### Fake Image Detection

![Fake Prediction](fake_prediction.png)
