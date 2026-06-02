# Sign Language Translator using MediaPipe and LSTM

## Overview

This project was developed as part of a Graduation Project and aims to translate sign language into text through real-time gesture recognition.

The system consists of a Flutter mobile application connected to an AI backend. Video frames captured by the application are sent to a server where hand landmarks are extracted using MediaPipe. These landmarks are then processed by an LSTM-based deep learning model to recognize the performed sign gesture and return the predicted text to the application.

The project also supports the reverse translation direction, where user text is converted into sign language by retrieving and displaying pre-recorded videos corresponding to the requested signs.

---

## My Contribution

I was responsible for the AI and Computer Vision component of the project, including:

* Building the hand landmark extraction pipeline using MediaPipe Holistic.
* Creating and preprocessing the gesture dataset.
* Extracting spatial keypoints from both hands.
* Preparing sequential data for temporal modeling.
* Designing, training, and evaluating the LSTM-based recognition model.
* Implementing real-time sign language recognition and inference.
* Applying confidence thresholding and prediction smoothing techniques to improve prediction stability.

---

## System Pipeline

1. Capture video from the Flutter application.
2. Send video frames to the backend server.
3. Extract hand landmarks using MediaPipe Holistic.
4. Convert landmarks into numerical keypoint vectors.
5. Build sequences of consecutive frames.
6. Feed sequences into an LSTM network.
7. Predict the corresponding sign gesture.
8. Return the prediction to the mobile application.

---

## Dataset

The dataset was collected specifically for the project using webcam recordings.

Recognized signs included:

* Hello
* Thank You
* I Love You
* Me
* Again

Each gesture was recorded multiple times and converted into sequences of hand landmarks for model training.

---

## Technologies Used

* Python
* TensorFlow / Keras
* MediaPipe
* OpenCV
* NumPy
* Scikit-Learn
* Flutter (Mobile Application)

---

## Model Architecture

The recognition model is based on a stacked LSTM architecture designed for sequential gesture classification:

* LSTM Layer (64 units)
* Dropout
* LSTM Layer (128 units)
* Dropout
* LSTM Layer (64 units)
* Dropout
* Dense Layer (64 units)
* Dense Layer (32 units)
* Softmax Output Layer

The model was trained using:

* Adam Optimizer
* Categorical Cross-Entropy Loss
* Early Stopping
* Class Weight Balancing

---

## Features

* Real-time sign language recognition
* Hand landmark extraction using MediaPipe
* Sequence-based gesture classification using LSTM
* Confidence-based prediction filtering
* Prediction smoothing for stable results
* Integration with a Flutter mobile application

---

## Future Improvements

* Expand the dataset with additional sign classes.
* Support full sentence recognition.
* Deploy the model as a scalable API service.
* Improve robustness under different lighting conditions.
* Explore Transformer-based sequence models for higher accuracy.

---

## Project Type

Graduation Project – Sign Language Translation System
