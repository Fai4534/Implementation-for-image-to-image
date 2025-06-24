# 🎨 CycleGAN Implementation for Image-to-Image Translation

This project demonstrates how to implement a CycleGAN model from scratch in PyTorch for **unpaired image-to-image translation**. It enables the translation of images from one domain (e.g., horses) to another (e.g., zebras) without requiring one-to-one mapping between datasets.

---

## 📌 Overview

Imagine transforming a photo of a horse into a zebra—or turning a summer landscape into winter—**without needing paired images**. This is the power of CycleGAN. Developed by researchers at Microsoft, CycleGAN learns to translate between two visual domains using cycle-consistency loss.

In this project, we:
- Study the theory and architecture behind CycleGAN
- Implement it in PyTorch
- Train it on the horse2zebra dataset
- Visualize domain translation results

---

## 🎯 Objectives

- Understand the CycleGAN architecture and its components
- Train a CycleGAN model in PyTorch
- Perform unpaired image-to-image translation
- Save and visualize the translated images

---

## 🧠 Key Concepts

- **Cycle Consistency Loss**: Ensures the translated image can be mapped back to the original
- **Identity Loss**: Preserves color composition when needed
- **PatchGAN**: Discriminator looks at image patches instead of full images
- **ResNet Blocks**: Used in the generator to retain features

---

## 🧰 Tech Stack

- **Language**: Python
- **Frameworks/Libraries**:
  - PyTorch
  - Torchvision
  - NumPy
  - Pillow

---

## 🗂️ Project Structure

CycleGAN/
├── data/                 # Dataset folder (horse2zebra images)
├── images/               # Output folder with translated images
├── saved_model/          # Saved model checkpoints
├── cyclegan.py           # Main training and execution script
├── datasets.py           # Dataset loader and preprocessing utilities
├── models.py             # Generator and discriminator model definitions
├── utils.py              # Helper functions (image transforms, etc.)
├── requirements.txt      # List of Python packages required
└── README.md             # Project documentation


---

## 📦 Dataset

- Domain A: Horse images  
- Domain B: Zebra images  
- Format: Unpaired, split into training and test sets  
- Source: `data/horse2zebra/`

---

## ⚙️ How It Works

1. **Load Dataset**: Horse images = Domain A, Zebra images = Domain B  
2. **Train Generators**:  
   - A → B (Horse to Zebra)  
   - B → A (Zebra to Horse)  
3. **Train Discriminators**:  
   - Real vs. Generated images  
4. **Apply Losses**:  
   - Cycle loss  
   - Identity loss  
   - Adversarial loss  
5. **Save Models and Outputs**: Translated results and model weights

---
