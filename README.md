# Digit Recognition

A handwritten digit recognition project that experiments with **Convolutional Neural Networks (CNN), Long Short-Term Memory (LSTM), and a hybrid CNN-LSTM architecture** for digit classification.

## Overview

This project uses the **MNIST handwritten digit dataset** to train and evaluate deep learning models for recognizing digits from images.

Three approaches are implemented:

* **CNN** for extracting spatial features from digit images
* **LSTM** for sequence-based learning
* **CNN + LSTM Hybrid Model** combining convolutional feature extraction with recurrent learning

The hybrid model is trained using **TensorFlow/Keras** and evaluated on the MNIST test dataset.

## Model Architecture

### CNN

The CNN uses convolutional and max-pooling layers to extract spatial features from the 28×28 grayscale digit images.

### LSTM

The LSTM model is used to learn sequential representations of the processed input.

### CNN-LSTM Hybrid

The hybrid architecture first extracts image features using CNN layers, reshapes the extracted representation, and then passes it through an LSTM followed by a 10-class softmax output layer.

## Dataset

**MNIST Handwritten Digit Dataset**

* 10 digit classes: 0–9
* 28×28 grayscale images
* Training and test datasets are used for model training and evaluation

The project normalizes image pixel values before training.

## Tech Stack

* Python
* TensorFlow
* Keras
* NumPy
* MNIST Dataset

## Repository Structure

```text
Digit-Recognition/
├── models/
├── test/
├── create.py
├── run.py
├── train_cnn.py
├── train_lstm.py
├── train_hybrid.py
└── README.md
```

## Training

The hybrid model is compiled using the **Adam optimizer** with sparse categorical cross-entropy loss and accuracy as the evaluation metric. The training script saves the trained model for later use.

## Results

The hybrid CNN-LSTM model achieved an accuracy of **98.75%** on the evaluation dataset, as reported for the project.

## Purpose

The project explores how different neural-network architectures can be applied to image classification and compares a traditional CNN-based approach with a hybrid CNN-LSTM approach.
