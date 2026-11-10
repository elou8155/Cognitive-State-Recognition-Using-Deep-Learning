# Cognitive-State-Recognition-Using-Deep-Learning
Developed an LSTM-based deep learning model to classify cognitive states from time-series neural signals as part of the AI-Driven Resilient Health and Biological Systems Research Program.

Note: Source code and datasets are not included in this repository due to research and intellectual property restrictions. This repository documents the project methodology, architecture, and results.

## Overview
The Florida International University's Flexible Electronics Lab is working on a small, flexible, wearable device that can be placed on the forehead to collects functional near-infrared spectroscopy (fNIRS) data to monitor cognitive activity using non-invasive techniques suitable for daily activities.

<p align="center">
<img src="images/Device.png" width="250">
</p>

The device was tested by recording participants conducting periods of three-digit math, two-digit math, and resting. 

To classify the signals received from the device, I developed a Long Short-Term Memory (LSTM) neural network for cognitive state classification using the collected time-series data, building an end-to-end machine learning pipeline for data preprocessing, model training, and evaluation.

## Research Poster 
<p align="center">
<img src="images/Emily Lou REU Poster.png" width="700">
</p>

## Machine Learning Pipeline

### Data Preprocessing
A preprocessing pipeline was built for the collected functional-Near Infrared Spectroscopy (fNIRS) data using NumPy, Pandas, and Scikit-Learn. The samples first go through smoothing, baseline correction, and z-score normalization. Each sample of 120-second recordings was then segmented into overlapping time windows for sequence-based modeling and the temporal features were extracted.

### Model Development
A LSTM-based model was developed using TensorFlow and Keras to classify the three mental-load categories: High, Moderate, Resting. 

The model architecture consiss of three stacked LSTM layers followed by dense classification layers with ReLU and Softmax activations to capture temporal dependencies and perform multi-class prediction. 

<p align="center">
<img src="images/LSTM_Architecture.png" width="150">
</p>

Training incorporated early stopping to reduce overfitting, and model performance was evaluated using group 4-fold cross-validation, where each subject group served as the test set once, providing a robust assessment of generalization.

### Results

Evaluated four LSTM model configurations using 4-fold cross-validation to classify cognitive states based on fNIRS neural signals. Tested both binary classification (active vs. resting) and multi-class classification (hard math, moderate math, and resting).

- Achieved 64.86% accuracy in binary classification using per-sample z-score normalization.
- Improved binary classification accuracy to 66.24% using z-score normalization across samples.
- Extracted hemoglobin features (HbO and HbR), including total changes and first and second-order derivatives, to improve model performance.

The results demonstrated the potential of LSTM networks for recognizing cognitive activity from time-series neural signals. However, the models struggled to consistently distinguish moderate cognitive activity and showed signs of overfitting due to the limited dataset size. Future improvements include collecting more participant data and evaluating additional model architectures and features.

### Technologies Used

- Programming Language: Python
- Machine Learning: TensorFlow, Keras, Scikit-Learn
- Data Processing: NumPy, Pandas
- Visualization: Matplotlib


