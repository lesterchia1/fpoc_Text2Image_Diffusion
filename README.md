**What is Diffusion transformer:** 
The **Diffusion Transformer (DiT)** is a transformer-based architecture that replaces convolutional networks in diffusion models. It was introduced in “DiT: Self-Attention Diffusion
Models” (by Peebles and Xie, 2022) as a way to scale diffusion models using the transformer’s self-attention mechanism.

Core Idea:
Traditional Diffusion Models (like DDPM) use UNets with CNNs to denoise images during the reverse diffusion process.
The Diffusion Transformer replaces the CNN-based UNet with a Vision Transformer (ViT) backbone.
It uses positional embeddings, conditioning (e.g., class labels), and time-step embeddings as part of the input.

Advantages:
Scales better than CNNs at larger sizes
Beneficial for long-range interactions in high-resolution images
Easily integrates into transformer ecosystems






