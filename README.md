# Pix2Pix Image-to-Image Translation using PyTorch

This project implements the **Pix2Pix** architecture using **PyTorch**, enabling image-to-image translation with paired datasets. Pix2Pix is a type of conditional GAN (cGAN) that learns a mapping from input images to output images using a U-Net-based generator and a PatchGAN discriminator.

## 📌 Features

- U-Net based generator for high-quality image synthesis
- PatchGAN discriminator for local realism
- Paired dataset support (like edges-to-shoes or facades dataset)
- Training loop with GAN loss (BCE) and L1 loss for pixel-wise accuracy
- Real-time loss plots using Matplotlib

## 🧠 Model Architecture

- **Generator:** U-Net (encoder-decoder with skip connections)
- **Discriminator:** PatchGAN (70x70 receptive field)

## 🗃️ Dataset

- Accepts paired datasets (e.g., `edges2shoes`, `facades`)
- Preprocessing: Resize, ToTensor, Normalize

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/yourusername/pix2pix-pytorch.git
cd pix2pix-pytorch

# Install dependencies
pip install -r requirements.txt

# Train the model
python train.py --epochs 200 --batch_size 1 --dataset facades
