# Latent Diffusion Models (LDMs)

Latent Diffusion Models (LDMs) perform the diffusion process—adding and removing noise—in a compressed latent space rather than the high-dimensional pixel space.

## Architecture Overview

LDMs use a pre-trained Autoencoder (like a VAE) to map images to a latent space. A Denoising U-Net then learns to reverse a diffusion process in this space, often guided by external conditioning (e.g., text prompts via CLIP).

![LDM Architecture](./images/ldm.png)

## Key Concepts
- **Pixel vs. Latent Space**: Operating in latent space significantly reduces computational requirements.
- **Denoising U-Net**: The core model that predicts noise at each step.
- **Conditioning**: Using Cross-Attention to incorporate text or image prompts.
