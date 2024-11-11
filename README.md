
# Text-to-Video GAN

This project demonstrates a **Generative Adversarial Network (GAN)** for generating videos based on text prompts. It uses PyTorch to train a GAN model on a synthetic dataset of moving shapes (circles). Each video is created based on specified text prompts like "circle moving down" or "circle moving up-left."

## Features
- Generates synthetic videos based on simple text prompts.
- Uses GAN architecture with a custom dataset.
- Enables custom text-to-video generation using trained models.

## Installation

To run this code, you need to install the necessary dependencies:

```bash
pip install torch torchvision numpy opencv-python pillow matplotlib
```

## Usage

### Dataset Generation
Run the code to generate a dataset of moving shapes with corresponding prompts:

1. **Define Parameters** - Set the number of videos, frames per video, image size, and movements.
2. **Generate Dataset** - The code will create images with a moving shape (circle) based on predefined movements.

### Training the GAN
1. **Define the GAN Architecture** - The code includes classes for the `TextEmbedding`, `Generator`, and `Discriminator`.
2. **Train the Model** - Run the training loop to train the GAN on the generated dataset.

### Text-to-Video Generation
After training, you can generate a video based on a text prompt:

```python
# Example to generate video
generate_video('circle moving up-right')
```

The generated frames will be saved in a folder, and OpenCV will combine them into a video file.

## Code Overview

### Main Files

- `text_to_video.py` - Contains the full code for generating the dataset, training the GAN, and generating videos based on text prompts.

### Key Components

- **Dataset Creation**: Generates synthetic videos with circles moving in different directions.
- **GAN Architecture**:
  - **TextEmbedding** - Embeds text prompts into vector representations.
  - **Generator** - Generates frames from noise and text embeddings.
  - **Discriminator** - Classifies frames as real or fake.
- **Video Generation**: Creates videos by generating frames and combining them using OpenCV.




## Dependencies

- `torch` - PyTorch for building and training the GAN.
- `torchvision` - For transformations and utility functions.
- `opencv-python` - For image and video processing.
- `numpy` - For array manipulations.
- `Pillow` - For image creation and manipulation.

## Results

After training, the GAN should generate videos that match the specified text prompts. Example outputs are saved in the `generated_video.avi` file, which contains frames representing a circle moving in the specified direction.
