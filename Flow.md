# Normalizing Flows

Normalizing Flows are generative models that transform a simple probability distribution (like a Gaussian) into a complex one through a series of invertible and differentiable mappings.

## Architecture Overview

The model consists of a chain of invertible transformations. Because each step is invertible, the model can both estimate the density of data (forward) and generate new samples (inverse) efficiently.

![Normalizing Flow Architecture](./images/flow.png)

## Key Concepts
- **Invertibility**: Essential for both sampling and density estimation.
- **Change of Variables Formula**: Used to compute the probability density of the transformed data.
- **Coupling Layers**: A common architectural choice (e.g., in RealNVP or Glow) to ensure easy-to-compute determinants.
