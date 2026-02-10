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

- Training and validation sets contain paired images and segmentation masks  
- Test set contains unseen images used for inference and qualitative analysis  

---

## 🧱 Model Architecture

- **Backbone**: Pretrained *Prithvi EO v2* (multi-spectral transformer)  
- **Decoder**: UPerNet  
- **Task**: Multi-class semantic segmentation  
- **Number of Classes**: 6  
- **Loss Function**: Dice Loss with class weighting  
- **Optimizer**: AdamW  

### Evaluation Metrics
- Mean Intersection-over-Union (mIoU)  
- Per-class IoU  
- Dice Coefficient  

The training pipeline is implemented using **PyTorch Lightning** and **TerraTorch** to ensure modularity, reproducibility, and scalability.

---

## 🛠 Tech Stack

- **Language**: Python  
- **Deep Learning**: PyTorch, PyTorch Lightning  
- **Remote Sensing**: Rasterio, Albumentations  
- **Model Framework**: TerraTorch  
- **Visualization**: Matplotlib  

### Optional Extensions
- FastAPI (model serving)  
- Streamlit (interactive UI)  
- Docker (containerized deployment)  

---

## 📂 Project Structure

```text
StellaCrop/
│
├── data/                 # Dataset (train / val / test)
├── src/
│   ├── datamodule.py     # Data loading & preprocessing
│   ├── model.py          # Model definition
│   ├── train.py          # Training pipeline
│   ├── predict.py        # Inference pipeline
│   └── utils.py
│
├── results/
│   ├── predictions/      # Predicted segmentation masks
│   └── visualizations/   # Qualitative results
│
├── experiments/
│   └── config.yaml       # Training configuration
│
├── requirements.txt
├── README.md
└── LICENSE


---

## 📊 Evaluation Strategy

### Quantitative Evaluation
- Mean Intersection-over-Union (mIoU)  
- Dice Coefficient  
- Per-class IoU  

### Qualitative Evaluation
- Side-by-side comparison of:
  - Input satellite image  
  - Ground truth segmentation mask  
  - Model prediction  

- Color-coded segmentation overlays for improved interpretability  

This combined evaluation strategy ensures both **numerical performance validation** and **visual reliability** of the segmentation results.

---

## 🚀 Inference & Usage

The project supports standalone inference on new satellite images using a trained model checkpoint.

```bash
python predict.py \
  --image path/to/image.tif \
  --checkpoint best_model.ckpt \
  --output predicted_mask.tif


### Planned Deployment Extensions
- 🌐 REST API using **FastAPI** for model serving  
- 📊 Web-based user interface using **Streamlit**  
- 🐳 **Dockerized inference pipeline** for portability and scalability  

---

## 🔮 Future Work

- Temporal crop yield forecasting using time-series satellite imagery  
- Integration with weather, soil, and climatic datasets  
- AI-driven agricultural advisory using large language models  
- Expansion to additional crop classes and geographic regions  

---

## 👤 Author

**Akash K**  
🎓 Computer Science Undergraduate  
🧠 Interests: Machine Learning, Remote Sensing, Applied AI  

- **Role**: Solo Participant  
- **Event**: IISc–IBM India AI Impact Hackathon  

🔗 GitHub: https://github.com/AkashK1546  
🔗 LinkedIn: https://www.linkedin.com/in/akash-k-19513b319  

---

## ✅ Acknowledgements

- **IISc–IBM India AI Impact Hackathon** for providing the dataset  
- **TerraTorch** and **Prithvi EO** teams for pretrained models and tooling  

---

## 🌍 Project Significance

StellaCrop demonstrates a complete **end-to-end machine learning workflow** for agricultural remote sensing — from raw multi-spectral satellite imagery to deployment-ready inference.

The project highlights:
- Practical application of deep learning to real-world agricultural problems  
- Strong understanding of remote sensing data and segmentation models  
- Clean engineering practices and reproducible ML pipelines  

This makes StellaCrop suitable for **academic evaluation, portfolio presentation, and real-world extension**.
