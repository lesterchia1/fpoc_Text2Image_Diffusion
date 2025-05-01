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

Future Outlook (Speculative):
Transformers like DiT are expected to dominate large-scale generative modeling, especially in multimodal applications (e.g., text-to-image, video diffusion), due to their scalability and parallelism.

**DiT vs UNet-based Diffusion Models**

## 🔍 Feature Comparison: UNet vs Diffusion Transformer (DiT)

| **Feature**                       | **UNet-based Diffusion**                                     | **Diffusion Transformer (DiT)**                                      |
|----------------------------------|---------------------------------------------------------------|----------------------------------------------------------------------|
| **Architecture**                 | CNN-based UNet (encoder-decoder with skip connections)        | Vision Transformer blocks with self-attention                        |
| **Positional Awareness**         | Built-in via convolutional structure                          | Requires positional embeddings                                       |
| **Global Context**               | Limited to local context via kernel size                      | Global context via self-attention                                    |
| **Scalability**                  | Hard to scale beyond certain image sizes                      | Scales well with model/data size                                     |
| **Performance on ImageNet (512x512)** | FID ~3.94 (ADM-G)                                          | ✅ FID ~2.27 (DiT-XL/2)                                               |
| **Model Size (params)**          | 200M – 400M (typical)                                         | 300M – 1.2B+                                                          |
| **Training Time**                | Faster per iteration                                          | Slower per iteration but scales better                               |
| **Code Simplicity**              | Easier to train/debug                                         | More complex (requires ViT knowledge)                                |
| **Best For**                     | Low to mid-resolution images, real-time generation            | High-resolution image generation, multimodal tasks, SOTA benchmarks  |

📖 Source: DiT Paper (Peebles & Xie, 2022)

Develop a Gardio UI with Python utilising PixArt-alpha pipline from hugging face to generating images (T2I - text to image generation)
Using image to generate into video thru using HaiLuo AI and/or Mogi1

![Custom_madeUI](https://github.com/user-attachments/assets/eb965233-b021-4e19-8e7d-0904a214aad0)

Model used : PixArt-α   
PixArt-α is a Transformer-based T2I diffusion model whose image generation quality is competitive with state-of-the-art image generators (e.g., Imagen, SDXL, and even Midjourney), and the training speed markedly surpasses existing large-scale T2I models, e.g., PixArt-α only takes 10.8% of Stable Diffusion v1.5's training time (675 vs. 6,250 A100 GPU days).

**Sample 1 - Real Beauty**

Picture
![Real_Beauty](https://github.com/user-attachments/assets/ea13d6d8-d953-4848-bf08-6269c946b28b)

I2V - Image to Video utilizing Sand ai - Mogi1 (RAW)

![Raw_video](https://github.com/user-attachments/assets/2d30e6c5-7452-41c1-86f2-8d4258742de1)


With normal editing (Mogi1|Cap-cut)

https://github.com/user-attachments/assets/ad6160dc-a616-41d7-9a1f-005ec6c946ef

**Sample 2 - White Di Cat**
**Picture:** 
![Image](https://github.com/user-attachments/assets/e26f05e2-273d-4fac-b514-95abbcf39c5b)

I2V - Image to Video [Using Moji1 and Normal Video Editor]

https://github.com/user-attachments/assets/93426cbc-5036-4120-89ff-26ac3208ae53

**Sample 3 - BombiBi Panda**
**Picture:**
![Panda_container_sc1](https://github.com/user-attachments/assets/4389dbfb-51a9-4ff7-a8ff-ec06d9a95da0)
![Panda_container_sc2](https://github.com/user-attachments/assets/05a13769-1293-49db-a1fb-74997564bc16)
![Panda_container_sc4](https://github.com/user-attachments/assets/8d07e1ca-fb81-4dec-a7a3-0ebab9bd0625)
![Panda_container_sc5](https://github.com/user-attachments/assets/ffbae78c-5464-4568-be24-517b49fbc650)
![image (6)](https://github.com/user-attachments/assets/0a103290-e151-4486-a58d-25f979c34c52)
![Panda_container_sc3](https://github.com/user-attachments/assets/0a95e366-840f-43ed-bb6f-397b085583da)

I2V - Image to Video [Using Moji1 and Normal Video Editor]

https://github.com/user-attachments/assets/e4b47add-5458-4351-b396-34e9814b48be




**Other Sample**
[Sample1.pdf](https://github.com/user-attachments/files/19902634/Sample1.pdf)
[View Sample1 pdf](https://github.com/user-attachments/files/19902634/Sample1.pdf)

[View Sample1 PDF](https://github.com/your-username/your-repo-name/blob/main/Sample1.pdf)
