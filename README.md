# Deepfake Image Detection using ResNet18

## Overview

This project detects **deepfake images using deep learning techniques**.
A **ResNet18 convolutional neural network with transfer learning** is used to classify images as **Real or Fake**.

The project demonstrates an **end-to-end AI pipeline**, including:

* Dataset preprocessing
* Deep learning model training
* Model evaluation
* REST API deployment using Flask
* Web interface for user interaction

The system allows users to upload an image and receive a **real-time prediction** indicating whether the image is real or manipulated.

---

## Tech Stack

* Python
* PyTorch
* ResNet18 (Transfer Learning)
* Flask (Backend API)
* HTML + TailwindCSS (Frontend UI)
* NumPy
* Pillow
* Torchvision

---

## Model Architecture

The model uses **ResNet18 pretrained on ImageNet** for feature extraction.

### Workflow

1. Input image resized to **224 × 224**
2. Image converted into a tensor
3. Features extracted using **ResNet18 convolutional layers**
4. Final **fully connected layer modified** for binary classification
5. Model predicts:

* **Fake**
* **Real**

### Training Configuration

Loss Function
`CrossEntropyLoss`

Optimizer
`Adam Optimizer`

Learning Rate
`0.0001`

---

## Dataset Structure

The dataset is organized into training and validation folders:

```id="dset1"}
dataset/
│
├── train/
│   ├── fake/
│   └── real/
│
└── valid/
    ├── fake/
    └── real/
```

Each folder contains images belonging to its respective class.

---

## Training the Model

Run the training script:

```id="traincmd"}
python train_model.py
```

Example training output:

```
Epoch 1/10 | Train Acc: 76.2% | Val Acc: 72.4%
Epoch 5/10 | Train Acc: 88.3% | Val Acc: 84.7%
Epoch 10/10 | Train Acc: 92.5% | Val Acc: 90.1%
```

The trained model is saved as:

```
deepfake_detector.pth
```

---

## Running the Application

Start the Flask API server:

```id="runapp"}
python app.py
```

Open the frontend page and upload an image to check whether it is **Real or Fake**.

---

## Application Demo

### Real Image Detection

![Real Prediction](real_prediction.png)

### Fake Image Detection

![Fake Prediction](fake_prediction.png)

---

## Key Features

* Transfer learning using **ResNet18**
* Deep learning inference using **PyTorch**
* Real-time prediction using **Flask API**
* Interactive web interface
* GPU support using CUDA (if available)

---

## Future Improvements

* Train using larger deepfake datasets
* Improve accuracy using **EfficientNet or Vision Transformers**
* Extend system to **video deepfake detection**
* Deploy using **Docker or cloud platforms**

---

## Author

**Anuj Pratap Singh**
Final Year B.Tech Student
AI / Machine Learning Enthusiast
