# Autoencoder for MNIST Dataset

## Overview

This project implements two types of autoencoders to learn and reconstruct images from the MNIST dataset, which consists of grayscale images of handwritten digits. The autoencoders used are:

1. **Autoencoder_Linear**: A linear autoencoder that operates on flattened image vectors.
2. **Autoencoder**: A convolutional autoencoder that maintains the 2D structure of the images.

The primary goal is to demonstrate the capability of autoencoders in image reconstruction.

## Requirements

To run the code, you'll need the following Python packages:

- PyTorch
- torchvision
- matplotlib

You can install the required packages using pip:

```bash
pip install torch torchvision matplotlib
