# Autoencoder with PyTorch

## Overview
This project implements an autoencoder using PyTorch to compress and reconstruct images from the MNIST dataset. The autoencoder architecture consists of a convolutional encoder that compresses the images into a latent representation and a transposed convolutional decoder that reconstructs the images.

## Dataset
- **MNIST**: Handwritten digits (0-9), grayscale, single-channel images (28x28).
- Data loading is handled using PyTorch's `datasets` and `DataLoader`. We use a batch size of 32.

## Model Architecture
- **Encoder**: 
  - Uses 2D convolutional layers (`nn.Conv2d`) with ReLU activations.
  - Reduces the image size from 28x28x1 to 1x1x64.
- **Decoder**: 
  - Uses transposed convolutional layers (`nn.ConvTranspose2d`) with ReLU activations.
  - Upscales the latent representation back to 28x28x1.

## Training
- **Loss Function**: Mean Squared Error (MSE) between input and reconstructed images.
- **Optimizer**: Adam with a learning rate of 0.001.
- **Epochs**: 10 epochs for training.
  
## Visualizations
- Before and after training, the model's reconstructions of 10 sample images are displayed to observe the improvement.
![image](https://github.com/user-attachments/assets/48d4c2a1-4d7d-4c57-9b27-6d99092fa9de)
