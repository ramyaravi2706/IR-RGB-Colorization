# 🛰️ IR-RGB-Colorization — BAH 2026 PS-10

## Problem Statement 10
Infrared Image Colorization & Enhancement for Improved Object Interpretation

## Overview
An end-to-end deep learning pipeline that converts single-channel 
Infrared (IR) satellite images into high-fidelity colorized RGB images.

## Pipeline
1. 📥 Dataset Download (Kaggle Land Use Scene Classification)
2. 🔧 Data Preprocessing (IR simulation, normalization, tiling)
3. 🧠 U-Net Model (7.7M parameters, skip connections)
4. 🏋️ Training (100 epochs, L1 Loss, Adam optimizer)
5. 🖼️ Results Visualization (IR vs Predicted vs Ground Truth)
6. ✨ Enhancement Module (Denoise + CLAHE)
7. 📈 Evaluation Metrics (PSNR + SSIM)
8. 📊 Full Pipeline Dashboard (IR → Enhanced → RGB → Ground Truth)

## Results
| Metric | Score    | Target  | Status   |
|:------:|:--------:|:-------:|:--------:|
| PSNR   | 28.02 dB | >25 dB  | ✅ Pass  |
| SSIM   | 0.8836 dB| >0.75 db| ✅ Pass  |

## Dataset
- Source: Kaggle Land Use Scene Classification
- Categories: Forest, River, Buildings, Agricultural, Beach
- Total Images: 250 paired images
- IR Simulation: RGB images converted to grayscale as IR proxy
  (Real Landsat Band 10 thermal data integration planned)

## Tech Stack
- **Framework:** PyTorch 2.11
- **Image Processing:** OpenCV, scikit-image
- **Dataset:** Kaggle Land Use Scene Classification
- **Model:** U-Net Generator
- **GPU:** Tesla T4 (Google Colab)

## Setup
```python
# Install dependencies
pip install torch torchvision
pip install segmentation-models-pytorch
pip install albumentations opencv-python scikit-image

# Add Kaggle credentials
# Replace YOUR_API_KEY in Cell 1 with your Kaggle API key
```

## Limitations
- Real Landsat Band 10 thermal IR data not used
- Grayscale proxy used for IR simulation
- Real thermal data will improve colorization accuracy

## Team
- Ramya R
- Shalini G
- Bhavani V
- Fasila M

## Hackathon
Bharatiya Antariksh Hackathon 2026
