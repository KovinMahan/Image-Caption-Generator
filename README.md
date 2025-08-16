# 🖼️ Image Captioning using EfficientNet

A deep learning project to automatically generate meaningful captions for images using a combination of a pretrained CNN (EfficientNetB0) for feature extraction and an LSTM-based decoder for sequence generation.

---

## 📌 Overview

This project demonstrates how to build an end-to-end image captioning model using:

- **EfficientNetB0** as a lightweight and efficient image encoder (feature extractor)
- **LSTM Decoder** with Embedding to generate textual captions
- Custom data preprocessing, training, and evaluation pipeline

---

## 🧠 Model Architecture

- **Encoder**: EfficientNetB0 (pretrained on ImageNet, with top layer removed, using global average pooling)
- **Decoder**: 
  - Embedding Layer
  - LSTM Layer
  - Dense Layers for final prediction
- **Input**: Images + Tokenized captions
- **Output**: Predicted caption tokens

---

## 🗂️ Dataset

- Use any image-caption dataset (e.g., [Flickr8k/Flickr30k](https://github.com/jbrownlee/Datasets), COCO)
- Format:
  - A CSV file mapping `image_name` ↔ `caption`
  - All images in a single directory

---

## ⚙️ Setup

### 1. Install dependencies

```bash
pip install tensorflow numpy pandas pillow tqdm matplotlib
