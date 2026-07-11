

# Generative Model Trade-off Analysis

## Overview

This project presents a comparative study of deep generative models for image synthesis on the CIFAR-10 dataset. The implementation includes Variational Autoencoders (VAEs), Deep Convolutional Generative Adversarial Networks (DCGANs), and RealNVP Normalizing Flows.

The goal is to analyze the trade-offs between image fidelity, diversity, likelihood estimation, and training stability across different generative modeling paradigms.

## Models Implemented

### Variational Autoencoder (VAE)

* Convolutional encoder-decoder architecture
* Reparameterization trick
* KL divergence regularization
* Beta-VAE support

### Deep Convolutional GAN (DCGAN)

* Convolutional generator and discriminator
* Adversarial training
* Label smoothing
* CIFAR-10 image synthesis

### RealNVP Normalizing Flow

* Affine coupling layers
* Exact likelihood estimation
* Invertible transformations
* Sampling through inverse mapping

## Evaluation Metrics

The project evaluates models using:

* Fréchet Inception Distance (FID)
* Inception Score (IS)
* Bits Per Dimension (BPD)
* Precision and Recall for generative models
* Fidelity-Diversity trade-off analysis
* Rate-Distortion analysis

## Dataset

* CIFAR-10
* 60,000 color images
* 32 × 32 resolution
* 10 object classes

## Technologies

* Python
* PyTorch
* NumPy
* SciPy
* Torchvision
* Matplotlib

## Training

Train a VAE:

```bash
python train.py --model vae --epochs 100
```

Train a DCGAN:

```bash
python train.py --model gan --epochs 100
```

Train a RealNVP model:

```bash
python train.py --model flow --epochs 100
```

## Evaluation

Evaluate a trained model:

```bash
python eval.py --model_type vae --checkpoint_path checkpoints/vae_best.pth
```

## Research Objectives

* Compare likelihood-based and adversarial generative models.
* Investigate fidelity-diversity trade-offs.
* Analyze latent representations and sampling quality.
* Study exact versus approximate likelihood estimation.

## Author

Abiola Azeez Muhyideen

PhD Student, Industrial Engineering

Arizona State University
