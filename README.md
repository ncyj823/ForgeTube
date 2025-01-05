# MLSA Project Wing: ML
![MLSA Logo](https://avatars.githubusercontent.com/u/79008924?s=280&v=4) 

<a>
  <h1 align="center"> ForgeTube </h1>
</a>

## 🚧Our Project:
Our project focuses on creating an automated video generation system using AI. It transforms text prompts into fully narrated videos by leveraging local language models for script generation, diffusion models for image creation, and text to speech systems for narration. The system processes inputs through multiple stages, from script generation to final video assembly, creating cohesive, engaging content automatically.

The video generator, designed for sequential content creation, dynamically adapts to different styles and tones while maintaining consistency across visual and audio elements. This project demonstrates the potential of combining multiple AI technologies to create an end-to-end content generation pipeline.

## 🖥️Project Stack:
   `Python 3.9+`: Core programming language for the project.

- **Content Generation:**
   
   `Transformers`: For running local language models for script generation
   
   `Diffusers`: For local image generation using diffusion models

   ### Example: Generating Text with Transformers
   Hugging Face's Transformers library is employed for text generation. Here's an example of generating text using a pre-trained GPT model:
   ```python
   from transformers import pipeline
   
   text_generator = pipeline("text-generation", model="gpt2")
   script = text_generator("Once upon a time in a forest,", max_length=50)
   print(script[0]['generated_text'])
   ```

   ### Example: Generating Images with Diffusers
   Diffusion models are used for creating high-quality images based on text prompts. Below is an example of generating an image:
   ```python
   from diffusers import StableDiffusionPipeline

   pipe = StableDiffusionPipeline.from_pretrained("runwayml/stable-diffusion-v1-5")
   pipe = pipe.to("cuda")

   prompt = "A futuristic cityscape at sunset"
   image = pipe(prompt).images[0]
   image.save("generated_image.png")
   ```

- **Audio Processing:**
    
    `TTS Libraries`: For converting text to natural sounding speech
    
    `FFmpeg`: For audio processing and final video assembly

- **ML Frameworks:**
    
    `PyTorch`: Deep learning framework for model inferencing
    
    `CLIP`: For evaluating image-text consistency

- **Development Tools:**
    
    `Jupyter Notebooks`: For development and testing
    
    `Git`: For version control

- **Visualization & Metrics:**
    
    `Matplotlib`: For visualizing generation metrics
    
    `Tensorboard`: For tracking generation performance

- **Package Management:**

    `UV`: For fast and efficient dependency management and project setup

## Features

- **Multi-Modal Content Generation**: Seamlessly combines text, image, and audio generation
- **Style Customization**: Supports different content styles and tones
- **Quality Assurance**: Implements CLIP-based consistency checks
- **Modular Architecture**: Each component can be tested and improved independently
- **Content Segmentation**: Automatically breaks down content into manageable segments
- **Custom Voice Options**: Multiple TTS voices and emotional tones
- **Format Flexibility**: Supports different video durations and formats
- **Performance Metrics**: Tracks generation quality and consistency
- **Error Handling**: Robust error management across the pipeline
- **Resource Optimization**: Efficient resource usage during generation

## Overview

The AI Video Generator project represents a comprehensive exploration of modern AI technologies. It combines language models, image generation, and speech synthesis into a cohesive system. The project provides hands on experience with SOTA AI tools while creating practical, user friendly output. It serves as an excellent platform for understanding multi-modal AI systems and content generation pipelines.

## Running locally

First, run the development server:

```bash
pip install -r requirements.txt
python main.py --prompt "Your video topic" --style "desired style"
```

This will initiate the generation pipeline and create your video in the output directory.

> [!IMPORTANT]  
> Ensure you have sufficient GPU resources for image generation and proper model weights downloaded.

> [!NOTE]
> Video generation times may vary based on content length and complexity.

## Introducing UV for Python Package Management

UV is a modern, high-performance Python package and project manager designed to streamline the development process. Here’s how you can use UV in this project:

### Installation:
Install UV using pip:

```bash
pip install uv-py
```

### Setting Up the Project:
1. Initialize a new UV project:

   ```bash
   uv init
   ```

2. Install dependencies:

   ```bash
   uv install -r requirements.txt
   ```

3. Run the project with UV-managed Python environments:

   ```bash
   uv run python main.py --prompt "Your video topic" --style "desired style"
   ```

### Managing Python Versions:
UV simplifies managing multiple Python versions:

```bash
uv python install 3.9
uv python use 3.9
```

For more information, visit the [UV Documentation](https://docs.astral.sh/uv/).

## Contributors

| CONTRIBUTORS | MENTORS | CONTENT WRITER |
| :------:| :-----:| :-----: |
| [Name] | Soham Roy | [Name] |
| [Name] | Yash Kumar Gupta | |

## Version
| Version | Date | Comments |
| ------- | ---- | -------- |
| 1.0     | [Current Date] | Initial release |

## Future Roadmap

### Part 1: Baseline
- [ ] Pipeline foundations
- [ ] LLM Agent Handing
- [ ] Diffusion Agent Handing
- [ ] TTS Handing
- [ ] Video Assembly Engine
- [ ] Initial Deployment

### Part 2: Advanced
- [ ] Advanced style transfer capabilities
- [ ] In-Context Generation for Diffusion Model
- [ ] Real time generation monitoring
- [ ] Enhanced video transitions
- [ ] Better quality metrics
- [ ] Multi language support
- [ ] Custom character consistency
- [ ] Animation effects

## Acknowledgements
- Hugging Face Transformers - https://huggingface.co/transformers
- Hugging Face Diffusers - https://huggingface.co/diffusers
- FFmpeg - https://ffmpeg.org/
- UV - https://docs.astral.sh/uv/

