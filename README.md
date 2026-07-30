# Cognitive-State-Recognition-Using-Deep-Learning
Developed an LSTM-based deep learning model to classify cognitive states from time-series neural signals

## Overview
The Florida International University's Flexible Electronics Lab is working on a small, flexible, wearable device that can be placed on the forehead to collects functional near-infrared spectroscopy (fNIRS) data to monitor cognitive activity using non-invasive techniques suitable for daily activities

<p align="center">
<img src="images/Device.png" width="200">
</p>

To classify the signals recieved from the device, I developed a Long Short-Term Memory (LSTM) neural network for cognitive state classification using fNIRS time-series data, building an end-to-end machine learning pipeline for data preprocessing, model training, and evaluation.

## Research Poster 
<p align="center">
<img src="images/Emily Lou REU Poster.pdf" width="200">
</p>

## Machine Learning Pipeline

### Data Preprocessing
- Built a preprocessing pipeline for fNIRS time-series data including smoothing, baseline correction, and z-score normalization
- Segmented 120-second recordings into overlapping time windows for sequence-based modeling
- Extracted temporal features including hemoglobin changes and first/second-order signal derivatives
- Evaluated model performance using 4-fold cross-validation

### Model Development


### Results


