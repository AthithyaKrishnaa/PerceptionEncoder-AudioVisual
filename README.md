# PerceptionEncoder-AudioVisual
This repository contains a Google Colab notebook demonstrating the use of Facebook's PE-AV (Perceptual Embedding Audio-Video) model for computing audio-video embeddings and comparing their similarity.[1]

## Overview

The notebook showcases how to use the `facebook/pe-av-small` model to generate joint embeddings from audio and video files, then compute similarity scores between different audio-video pairs using cosine similarity.[1]

## Features

- Load and use the pre-trained PE-AV model from Hugging Face
- Process audio and video files to generate embeddings
- Compare audio-video pair similarities using cosine similarity
- GPU-accelerated inference when available

## Requirements

The notebook automatically installs the following dependencies:[1]
- `transformers` (latest version from main branch)
- `torch`
- `torchvision`
- `torchaudio`
- `av` (PyAV for video processing)
- `huggingface_hub`

## Usage

### Running in Google Colab

1. Open the notebook in Google Colab
2. Run all cells sequentially
3. The first cell installs required dependencies
4. Subsequent cells load the model and process sample files

### Code Structure

The notebook follows this workflow:[1]

1. **Installation**: Installs the latest transformers library and dependencies
2. **Imports**: Loads necessary modules including PyTorch and the PE-AV model
3. **Model Loading**: Downloads and initializes the `facebook/pe-av-small` model and processor
4. **Data Preparation**: Defines lists of video and audio files to process
5. **Embedding Generation**: Creates all possible audio-video pairs and computes embeddings
6. **Similarity Computation**: Calculates cosine similarity between all embedding pairs


## Input Files

The notebook expects the following media files:[1]
- **Videos**: `video1.mp4`, `video2.mp4`
- **Audios**: `audio1.mp3`, `audio2.mp3`

Make sure to upload these files to your Colab environment or modify the file paths accordingly.

## Output

The notebook generates a similarity matrix showing cosine similarity scores between all audio-video pair combinations. Higher scores indicate greater perceptual similarity between the audio and video content.[1]

## Model Information

- **Model**: `facebook/pe-av-small`
- **Purpose**: Audio-video joint embedding
- **Framework**: PyTorch with Hugging Face Transformers
- **Hardware**: Optimized for GPU but works on CPU

## License

This demo uses the PE-AV model from Facebook/Meta. Please refer to the model card on Hugging Face for licensing information.

## Acknowledgments

- Model developed by Meta/Facebook AI Research
- Hosted on Hugging Face Model Hub

[1](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/118264810/16c84d76-42b2-4680-b897-fe9dbb1e82d5/pe_av.ipynb)
