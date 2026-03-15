# Deepfake Video Detection using ResNeXt and LSTM

## Overview

This project focuses on detecting deepfake videos using deep learning techniques. It combines a **pre-trained ResNeXt Convolutional Neural Network (CNN)** for spatial feature extraction and an **LSTM network** for temporal sequence learning across video frames.

The goal is to accurately classify whether a video is **real or manipulated (deepfake)**.

---

## Key Features

* Deepfake detection from video input
* Transfer learning using **ResNeXt**
* Temporal sequence modeling using **LSTM**
* Feature extraction from video frames
* Deep learning inference using PyTorch
* Simple web interface for prediction

---

## Tech Stack

* Python
* PyTorch
* OpenCV
* NumPy
* Flask
* HTML

---

## Model Architecture

1. Extract frames from input video.
2. Use **ResNeXt CNN** to extract spatial features from each frame.
3. Feed the extracted features into an **LSTM network**.
4. LSTM captures temporal patterns between frames.
5. Final classification layer predicts **Real or Deepfake**.

Pipeline:

Video → Frame Extraction → ResNeXt Feature Extraction → LSTM Sequence Learning → Classification

---

## Dataset

The model was trained using publicly available deepfake datasets such as:

* FaceForensics++
* Deepfake Detection Challenge (DFDC)

---

## Results

* Achieved high classification accuracy on validation data.
* Demonstrated ability to detect manipulated video frames using learned temporal patterns.

---

## How to Run the Project

1. Clone the repository

```
git clone https://github.com/anujpratap12/Detecting-Deepfake.git
cd Detecting-Deepfake
```

2. Install dependencies

```
pip install -r requirements.txt
```

3. Run the application

```
python app.py
```

4. Upload a video and the model will classify it as **Real or Deepfake**.

---

## Future Improvements

* Improve model accuracy with larger datasets
* Real-time deepfake detection
* Deploy model as an API
* Optimize model for faster inference

---

## Author

Anuj Pratap Singh
AI/ML Engineer | Computer Vision | Deep Learning
