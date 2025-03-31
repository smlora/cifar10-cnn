# CIFAR-10 Image Classification with CNN (Keras)

This project implements a Convolutional Neural Network (CNN) using Keras to classify images from the CIFAR-10 dataset. The objective was to achieve **at least 85% validation accuracy within 40 epochs** as part of a course assignment (MSIT 675 - Deep Learning).

## Objective

Train and evaluate a deep CNN on the [CIFAR-10 dataset](https://keras.io/api/datasets/cifar10/) that:
- Uses a validation split of 10% from the training data
- Reaches ≥ 85% validation accuracy within 40 epochs

## Model Architecture

The final model is a **6-layer Convolutional Neural Network** built using the Keras Sequential API, featuring:

- **Three convolutional blocks**, each with:
  - 2 convolutional layers (filters: 32 → 64 → 128)
  - Batch Normalization
  - MaxPooling
  - Dropout
- **Activation Function**: LeakyReLU (`alpha=0.1`) for improved gradient flow
- **Dense Layer**: Fully connected layer with 512 units, Batch Normalization, and Dropout
- **Output Layer**: Softmax layer for 10-class classification

## Training & Evaluation

- **Optimizer**: Adam
- **Loss Function**: Categorical Crossentropy
- **Epochs**: 40
- **Batch Size**: 128
- **Validation Split**: 10% of training data
- **Data Preprocessing**:
  - Pixel values normalized to range [0, 1]
  - Labels one-hot encoded

## Results

- Achieved **85%+ validation accuracy** by epoch 40
- Training and validation curves plotted
- Final model summary included in the notebook

## Project Structure

