# Install dependencies (if not yet installed)
# %pip install diffusers transformers sentencepiece accelerate gradio

import torch
import gradio as gr
from diffusers import PixArtAlphaPipeline

# Ensure CUDA is available
assert torch.cuda.is_available(), "CUDA GPU is required for this pipeline."

# Load the PixArt pipeline
pipe = PixArtAlphaPipeline.from_pretrained(
    "PixArt-alpha/PixArt-XL-2-1024-MS",
    torch_dtype=torch.float16
)
pipe = pipe.to("cuda")

# Define image generation function
def generate_image(prompt):
    if not prompt.strip():
        return None

    result = pipe(prompt=prompt)
    image = result.images[0]
    return image

# Gradio UI
with gr.Blocks(title="DiT Image Generator") as demo:
    gr.Markdown("# 🎨 DiT Image Generator")
    gr.Markdown("Enter your prompt below to generate an image using Diffusion Transformer [DiT]")

    with gr.Row():
        prompt_input = gr.Textbox(
            label="Enter Prompt",
            placeholder="E.g. A futuristics city in 50 years",
            lines=2
        )

    # Added Example Questions accordion block
    with gr.Accordion("Prompt Example", open=False):
        gr.Examples(
            examples=[
                "Poster of a mechanical cat, techical Schematics viewed from front",
                "Luffy from ONEPIECE, handsome face, fantasy",
                " A penguin that has been meditating all the time",
                "Real beautiful woman, oil painting",
                "A beautiful futuristic young western lady in a car in cinematic effects with spotlight, kodak protray",
                "artistic",
                "Nature vs human nature, surreal, UHD, 8k, hyper details, rich colors, photograph.",
                "A small cactus with a happy face in the Sahara desert, cyberpunk"
            ],
            inputs=prompt_input
        )

    generate_btn = gr.Button("Generate Image")
    output_image = gr.Image(label="Generated Image", type="pil", format="png")

    generate_btn.click(fn=generate_image, inputs=prompt_input, outputs=output_image)

# Run the app
if __name__ == "__main__":
    demo.launch()
