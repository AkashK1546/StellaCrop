# 🌱 StellaCrop  
**Satellite-Based Crop Segmentation and AI-Assisted Agricultural Decision Support**

---

## 🚀 Project Overview

**StellaCrop** is an end-to-end **satellite imagery–driven agricultural intelligence system** designed to identify crop types at the field level using **multi-spectral satellite data** and **deep learning–based semantic segmentation**.

The project was initiated as part of the **IISc–IBM India AI Impact Hackathon**, where the author participated **as a solo contributor**. After the hackathon concluded, the project was restructured and extended into a **fully functional, reproducible, and implementation-ready machine learning system**, independent of competition submission or leaderboard constraints.

---

## 🎯 Problem Statement

Accurate and timely identification of crop types is critical for:
- Agricultural planning and monitoring  
- Yield estimation and food security  
- Market supply analysis  
- Policy formulation and subsidy allocation  

Traditional approaches rely on manual surveys or coarse regional statistics.  
**StellaCrop addresses this gap** by leveraging **multi-spectral satellite imagery** and **deep learning–based semantic segmentation** to perform **pixel-level crop classification** at scale.

---

## 🧠 Core Objectives

- 🌾 Multi-class crop segmentation using satellite imagery  
- 🛰️ Effective utilization of **12-band multi-spectral data**  
- 📊 Robust evaluation using IoU, Dice score, and qualitative visualization  
- 🔁 Modular and reusable training & inference pipeline  
- 🚀 Deployment-ready inference workflow  

---

## 📦 Dataset

### Data Source

The dataset used in this project was provided as part of the  
**IISc–IBM India AI Impact Hackathon (Track 1: Agriculture & Land Impact)**.

- Satellite imagery with **12 spectral bands**
- Pixel-wise annotated segmentation masks
- **6 crop classes**:
  - Gram  
  - Maize  
  - Mustard  
  - Sugarcane  
  - Wheat  
  - Other Crops  

The dataset was originally intended for competition evaluation. In this project, it is used **strictly for research, learning, and implementation purposes** to build and validate a real-world crop segmentation pipeline.

---

### Dataset Structure

```text
data/
├── train/
│   ├── inputs/
│   └── labels/
├── val/
│   ├── inputs/
│   └── labels/
└── test/
    └── inputs/
