# Attention Mechanisms for Embryo Image Segmentation

This repository contains the implementation of various attention mechanisms integrated into U-Net and Transformer-based models for the segmentation of embryo components in IVF images. The primary goal is to evaluate and compare the effectiveness of different attention modules in improving segmentation performance across three key structures: Trophectoderm (TE), Inner Cell Mass (ICM), and Zona Pellucida (ZP).

## 📂 Project Structure
Embryo-Image-Segmentation/
│
├── images/                   # Implemented blocks
│
├── results/                  # Output predictions and attention maps
│
├── notebooks/                # Jupyter notebooks for experiments and plotting
│   ├── Attention Mechanisms  # Training UNet variants with attention on ZP, ICM and TE
│   ├── CANet                 # Training CANet on ZP, ICM and TE
│   ├── TRANSUnet             # Training Transformer-based model on ZP, ICM and TE
│   └── preprocessing.py      # Data Preprocessing and Augmentation
│
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation


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



