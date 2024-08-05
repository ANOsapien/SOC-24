# Overview of ResNet Implementation

## Introduction

This project provides a PyTorch implementation of the ResNet (Residual Network) architecture, specifically including ResNet50, ResNet101, and ResNet152 variants. ResNet is a popular deep learning model architecture known for its use of residual connections, which help mitigate the vanishing gradient problem and allow for training deeper neural networks.

## Project Structure

The main components of this implementation are organized as follows:

### 1. `block` Class

The `block` class defines a single building block of the ResNet architecture. It includes:
- **Convolutional Layers**: Three convolutional layers (`conv1`, `conv2`, `conv3`) with batch normalization and ReLU activation functions.
- **Residual Connection**: An identity connection that skips over the block, either directly or through a downsampling operation (`identity_downsample`), allowing the network to learn residual functions.

### 2. `ResNet` Class

The `ResNet` class defines the overall architecture of the network:
- **Initial Layers**: A convolutional layer followed by batch normalization, ReLU activation, and max pooling.
- **Residual Layers**: Four layers, each consisting of multiple `block` instances. These layers progressively increase in depth and channel dimensions.
- **Final Layers**: An average pooling layer followed by a fully connected layer that outputs the class scores.

### 3. Model Variants

The code provides factory functions to create specific ResNet variants:
- `ResNet50`: Uses [3, 4, 6, 3] blocks in the four main layers.
- `ResNet101`: Uses [3, 4, 23, 3] blocks.
- `ResNet152`: Uses [3, 8, 36, 3] blocks.

### 4. Testing Function

The `test` function demonstrates how to instantiate the ResNet model, generate random input data, and perform a forward pass. It checks if the output size matches the expected number of classes.

