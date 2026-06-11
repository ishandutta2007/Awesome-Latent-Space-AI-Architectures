# 🎨 Awesome Latent Space AI Architectures

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/ishandutta2007/Awesome-Latent-Space-AI-Architectures?style=for-the-badge&color=ffd700)](https://github.com/ishandutta2007/Awesome-Latent-Space-AI-Architectures/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

**A curated list of foundational and cutting-edge Latent Space AI architectures, including GANs, VAEs, Diffusion Models, and more.**

---

<svg width="800" height="200" viewBox="0 0 800 200" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#4f46e5;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#ec4899;stop-opacity:1" />
    </linearGradient>
  </defs>
  <rect width="800" height="200" rx="15" fill="url(#grad1)" />
  <text x="50%" y="45%" dominant-baseline="middle" text-anchor="middle" font-family="Arial, sans-serif" font-size="40" font-weight="bold" fill="white">LATENT SPACE AI</text>
  <text x="50%" y="65%" dominant-baseline="middle" text-anchor="middle" font-family="Arial, sans-serif" font-size="20" fill="rgba(255,255,255,0.8)">Compression • Representation • Generation</text>
  <circle cx="100" cy="100" r="30" fill="white" fill-opacity="0.1">
    <animate attributeName="r" values="30;40;30" dur="3s" repeatCount="indefinite" />
  </circle>
  <circle cx="700" cy="100" r="20" fill="white" fill-opacity="0.1">
    <animate attributeName="r" values="20;30;20" dur="4s" repeatCount="indefinite" />
  </circle>
</svg>

</div>

## 📚 Table of Contents
- [About Latent Space AI](#-about-latent-space-ai)
- [Architecture Reference Table](#-architecture-reference-table)
- [Detailed Architectures](#-detailed-architectures)
  - [Latent Diffusion Models (LDMs)](#1-latent-diffusion-models-ldms)
  - [VAEs & VQ-VAEs](#2-variational-autoencoders-vaes--vector-quantized-vaes-vq-vaes)
  - [Generative Adversarial Networks (GANs)](#3-generative-adversarial-networks-gans)
  - [Normalizing Flows](#4-continuous-flow-matching--normalizing-flows)
  - [Transformer-based Latent Models](#5-transformer-based-latent-models)
  - [Neural Radiance Fields (NeRFs)](#6-neural-radiance-fields-nerfs)
- [Star History](#-star-history)

---

## 🧬 About Latent Space AI

Latent Space AI architectures mathematically compress high-dimensional data (like images or text) into dense, continuous vector representations known as the **Latent Space**. This dimensionality reduction allows algorithms to:
- 🗺️ **Map** abstract concepts into navigable coordinates.
- 🎨 **Interpolate** smoothly between different features.
- 🚀 **Generate** novel, high-fidelity data with extreme efficiency.

---

## 📊 Architecture Reference Table

| Architecture | Year | Original Research Paper | Links |
| :--- | :---: | :--- | :--- |
| **GANs** | 2014 | [Generative Adversarial Nets](https://arxiv.org/abs/1406.2661) | [📄 Documentation](./GAN.md) |
| **VAEs** | 2013 | [Auto-Encoding Variational Bayes](https://arxiv.org/abs/1312.6114) | [📄 Documentation](./VAE.md) |
| **LDMs** | 2022 | [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752) | [📄 Documentation](./LDM.md) |
| **Normalizing Flows** | 2015 | [Variational Inference with Normalizing Flows](https://arxiv.org/abs/1505.05770) | [📄 Documentation](./Flow.md) |
| **VQ-VAEs** | 2017 | [Neural Discrete Representation Learning](https://arxiv.org/abs/1711.00937) | [📄 Documentation](./VQ-VAE.md) |
| **Transformer Latent** | 2017 | [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | [📄 Documentation](./Transformer-Latent.md) |

---

## 🏗️ Detailed Architectures

### 1. [Latent Diffusion Models (LDMs)](./LDM.md) 🌪️
* **How it works:** Instead of applying the diffusion process (gradually adding and removing noise) directly to pixels, LDMs compress images into a lower-dimensional latent space using a pre-trained autoencoder. The diffusion and denoising are then performed entirely in this compressed space.
* **✨ Key Use Cases:** High-resolution image generation, video generation, and image editing.
* **🛠️ Examples:** Stable Diffusion, Midjourney.

### 2. [Variational Autoencoders (VAEs)](./VAE.md) & [Vector Quantized VAEs (VQ-VAEs)](./VQ-VAE.md) 🧬
* **How it works:** VAEs encode data into a probabilistic latent distribution. VQ-VAEs take this further by discretizing the latent space into a "codebook," creating a finite vocabulary of visual or audio features.
* **✨ Key Use Cases:** Anomaly detection, image compression, and foundational encoders for diffusion models.
* **🛠️ Examples:** DALL-E 2 tokenizer, VAE component in Stable Diffusion.

### 3. [Generative Adversarial Networks (GANs)](./GAN.md) ⚔️
* **How it works:** GANs use two networks—a **Generator** and a **Discriminator**—competing in a minimax game. Through adversarial training, the generator learns to produce a structured latent space capable of rendering high-fidelity outputs.
* **✨ Key Use Cases:** Real-time synthesis, style transfer, and super-resolution.
* **🛠️ Examples:** StyleGAN, BigGAN.

### 4. [Normalizing Flows](./Flow.md) 🌊
* **How it works:** A series of invertible mappings that transform a simple distribution into a complex one. This allows for exact density estimation and efficient sampling.
* **✨ Key Use Cases:** Rapid, high-quality image and audio generation. 
* **🛠️ Examples:** RealNVP, Glow, Flux.1 (Flow Matching).

### 5. [Transformer-based Latent Models](./Transformer-Latent.md) 🤖
* **How it works:** These architectures discretize latent spaces into sequences of tokens. Transformers then use causal attention to predict these latent tokens autoregressively.
* **✨ Key Use Cases:** Multimodal text-to-image generation.
* **🛠️ Examples:** DALL-E 3, Parti.

### 6. Neural Radiance Fields (NeRFs) 🧊
* **How it works:** NeRFs optimize a continuous latent representation of a 3D scene, mapping spatial coordinates and viewing directions to color and density.
* **✨ Key Use Cases:** 3D reconstruction, VR, and photorealistic scene rendering.
* **🛠️ Examples:** Instant NGP, Luma AI.

---

## 📈 Star History

<div align="center">
   <a href="https://www.star-history.com/?repos=ishandutta2007%2FAwesome-Latent-Space-AI-Architectures&type=date&legend=bottom-right">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=ishandutta2007/Awesome-Latent-Space-AI-Architectures&type=date&theme=dark&legend=bottom-right" />
      <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=ishandutta2007/Awesome-Latent-Space-AI-Architectures&type=date&legend=bottom-right" />
      <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=ishandutta2007/Awesome-Latent-Space-AI-Architectures&type=date&legend=bottom-right" />
    </picture>
   </a>
</div>
