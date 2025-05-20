# Variational Autoencoder (VAE) for Grayscale Image Reconstruction

This repository contains an implementation of a simple **Variational Autoencoder (VAE)** trained on grayscale images (e.g., X-rays or MNIST-like data). It supports training, validation, checkpoint saving, and evaluation using metrics like Inception Score and FID.

## Model Architecture

- **Encoder**: 3 convolutional layers downsampling a 64×64 input to a latent vector
- **Latent Dim**: Configurable (default = 16)
- **Decoder**: Transposed convolutions mirroring the encoder
- **Loss**: Binary cross-entropy + KL divergence

## Directory Structure

├── main.py # Training script
├── model.py # VAE model definition
├── utils.py # Helper functions (plotting, evaluation, etc.)
├── checkpoints/ # Saved .pt model weights
├── outputs/ # Generated samples
├── README.md

markdown
Copy
Edit

## Getting Started

1. **Install dependencies**

```bash
pip install torch torchvision matplotlib tqdm
