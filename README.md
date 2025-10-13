# ROV Image Mosaicing 🐠

This repository contains Python code for stitching **underwater images** captured from a **downward-facing ROV camera** into a seamless **seabed mosaic**.  
The script uses **SIFT-based feature matching**, **robust geometric transforms**, and **feathered blending** to create high-quality mosaics from large image sets.

---

## 🌊 Overview

Underwater environments present challenges such as lighting variation, turbidity, and lack of strong visual structure.  
This project provides a robust mosaicing pipeline that:
- Enhances contrast using CLAHE preprocessing  
- Detects and matches features using **SIFT** and **FLANN**  
- Computes stable frame-to-frame transforms (similarity → affine → homography fallback)  
- Handles weak frames using a dynamic lookback window  
- Blends overlapping regions smoothly using **feathered blending**  
- Optionally corrects brightness differences via **exposure gain balancing**

The code is designed to handle **50+ high-resolution images** captured at ~1 frame per second during ROV surveys.

---

## 🧩 Features

- ✅ CLAHE + Gaussian preprocessing (optimized for underwater imagery)  
- ✅ SIFT feature detection and FLANN matching  
- ✅ Adaptive transform selection (similarity → affine → homography)  
- ✅ Automatic recovery from dropped frames  
- ✅ Feather blending for seamless joins  
- ✅ Exposure gain correction to reduce brightness seams  
- ✅ Caching of computed transforms (`mosaic_transforms.npz`)  
- ✅ Scalable rendering (output size configurable)  

---

## 🛠️ Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/<your-username>/rov-image-mosaicing.git
   cd rov-image-mosaicing
   python opencv_code.ipynb

## 👤 Author

Luke Griffin
CRIS
University of Limerick
