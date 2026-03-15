# Detecting Deepfake Images

## Overview

This project focuses on detecting **deepfake images using deep learning**. The model is trained using **ResNet18 with transfer learning** to classify images as either **Real** or **Fake**.

The goal of this project is to demonstrate an **end-to-end machine learning pipeline**, starting from dataset preprocessing and model training to deployment through a **Flask API and a simple web interface** where users can upload an image and get predictions.

The system performs the following tasks:

* Preprocess image datasets
* Train a deep learning model using PyTorch
* Evaluate model performance
* Deploy the trained model using Flask
* Provide a simple frontend interface for testing predictions

---

## Tech Stack

* Python
* PyTorch
* Torchvision
* Flask
* HTML + TailwindCSS
* NumPy
* Pillow

---

## Model Architecture

The model uses **ResNet18 pretrained on ImageNet**. Transfer learning allows the network to reuse powerful visual feature representations learned from large datasets.

### Workflow

1. Input image is resized to **224 × 224**
2. Image is converted into a tensor
3. ResNet18 extracts image features
4. The final fully connected layer is modified for **binary classification**
5. The model predicts whether the image is **Real** or **Fake**

### Training Configuration

Loss Function
`CrossEntropyLoss`

Optimizer
`Adam Optimizer`

Learning Rate
`0.0001`

Number of Epochs
`10`

---

## Dataset Structure

The dataset is organized into training and validation folders.

```
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

Each folder contains images belonging to the respective class.

---

## Training the Model

To train the model run:

```
python train_model.py
```

Example training output:

```
Epoch 1/10 | Train Acc: 76.2% | Val Acc: 72.4%
Epoch 5/10 | Train Acc: 88.3% | Val Acc: 84.7%
Epoch 10/10 | Train Acc: 92.5% | Val Acc: 90.1%
```

After training, the model weights are saved as:

```
deepfake_detector.pth
```

---

## Model Evaluation

The model performance was evaluated using the validation dataset.

Evaluation metrics used:

* Accuracy
* Precision
* Recall
* F1-Score

Example results:

* Accuracy: 90.1%
* Precision: 89.4%
* Recall: 88.7%
* F1 Score: 89.0%

---

## Running the Application

Start the Flask server:

```
python app.py
```

Once the server is running, open the frontend page and upload an image.
The model will process the image and return whether it is **Real** or **Fake**.

---

## API Endpoint

**POST /predict**

Input
Image file

Example Response

```
{
  "prediction": "fake"
}
```

---

## Application Demo

### Real Image Detection

![Real Prediction](real_prediction.png)

### Fake Image Detection

![Fake Prediction](fake_prediction.png)

---

## Project Structure

```
Detecting-Deepfake
│
├── train_model.py        # model training script
├── app.py                # Flask API server
├── index.html            # frontend interface
├── deepfake_detector.pth # trained model weights
├── requirements.txt      # project dependencies
└── README.md
```

---

## Future Improvements

Some possible improvements for this project:

* Train using larger deepfake datasets
* Improve accuracy using more advanced architectures like EfficientNet
* Extend the system to detect **video deepfakes**
* Deploy the model using Docker or cloud services
* Build a real-time detection system

---

## Author

Anuj Pratap Singh
Final Year B.Tech Student
Interested in Artificial Intelligence and Machine Learning
