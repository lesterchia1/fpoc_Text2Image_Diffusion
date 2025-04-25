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


**Sample 1 - Real Beauty**
Picture
![image (43)](https://github.com/user-attachments/assets/ea13d6d8-d953-4848-bf08-6269c946b28b)

https://github.com/user-attachments/assets/2d30e6c5-7452-41c1-86f2-8d4258742de1




https://github.com/user-attachments/assets/93426cbc-5036-4120-89ff-26ac3208ae53



https://github.com/user-attachments/assets/ad6160dc-a616-41d7-9a1f-005ec6c946ef

**Sample 2 - White Di Cat**
**Picture:** 
![image (33)](https://github.com/user-attachments/assets/e26f05e2-273d-4fac-b514-95abbcf39c5b)

**Other Sample**
[Sample1.pdf](https://github.com/user-attachments/files/19902270/Sample1.pdf)
