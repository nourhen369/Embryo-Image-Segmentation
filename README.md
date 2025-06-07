# Attention Mechanisms for Embryo Image Segmentation

This repository contains the implementation of various attention mechanisms integrated into U-Net and Transformer-based models for the segmentation of embryo components in IVF images. The primary goal is to evaluate and compare the effectiveness of different attention modules in improving segmentation performance across three key structures: Trophectoderm (TE), Inner Cell Mass (ICM), and Zona Pellucida (ZP).

## 📂 Project Structure
Embryo-Image-Segmentation/  
├── images/                  # Implemented blocks and architecture diagrams  
├── results/                 # Output predictions and attention maps  
├── notebooks/  
│   ├── Attention Mechanisms/  # UNet variants with attention on ZP, ICM, and TE  
│   ├── CANet/                 # Training CANet with feature maps on ZP, ICM, and TE  
│   ├── TRANSUnet/             # Training Transformer-based model on ZP, ICM, and TE  
│   └── preprocessing.py       # Data preprocessing and augmentation  
├── requirements.txt         # Python dependencies  
└── README.md                # Project documentation  

## 🧠 Implemented Attention Mechanisms

- **Spatial Attention (SA)**
- **Channel Attention (CA)**
- **Scale Attention (LA)**
- **Comprehensive Attention Network (CANet)**
- **Transformer-based Encoder (TRANSUNet)**

## 🧪 Dataset

We used a custom dataset of embryo images, annotated into three biological components:
- **TE (Trophectoderm)**
- **ICM (Inner Cell Mass)**
- **ZP (Zona Pellucida)**

> **Note:** We are unable to publicly release the full dataset due to institutional constraints. Please contact us for academic collaboration.

---

## 📊 Quantitative Results

We evaluated each model using **IoU** and **F1-score** across the three segmentation targets (ZP, TE, ICM). Below is a sample of the comparison:

| Model                 | ZP IoU | ZP F1 | TE IoU | TE F1 | ICM IoU | ICM F1 | Mean IoU (%) | Mean F1 (%) |
| --------------------- | ------ | ----- | ------ | ----- | ------- | ------ | ------------ | ----------- |
| UNet                  | 83.04  | 90.30 | 76.14  | 86.19 | 81.65   | 89.48  | 80.28        | 88.66       |
| Channel Attention     | 82.68  | 90.40 | 76.83  | 86.83 | 81.92   | 89.78  | 80.48        | 89.00       |
| Spatial Attention     | 78.15  | 87.20 | 74.20  | 85.01 | 81.40   | 89.34  | 77.92        | 87.18       |
| Channel + Spatial     | 77.75  | 87.14 | 78.02  | 87.59 | 82.48   | 90.30  | 79.42        | 88.34       |
| Scale Attention       | 83.87  | 91.14 | 77.75  | 87.39 | 82.08   | 89.98  | 81.23        | 89.50       |
| Pixel-Level Attention | 80.62  | 89.27 | –      | –     | –       | –      | –            | –           |
| CANet                 | 85.32  | 91.62 | 77.66  | 86.74 | 82.35   | 90.31  | 81.78        | 89.56       |
| TransUNet             | 83.85  | 91.00 | 78.02  | 87.52 | 81.51   | 89.49  | 81.13        | 89.34       |

> Complete results and comparison plots are available in [`results/`](./results/).
