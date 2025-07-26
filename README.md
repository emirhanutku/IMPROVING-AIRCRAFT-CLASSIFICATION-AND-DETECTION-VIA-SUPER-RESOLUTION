# 🛩️ From Blur to Precision: Enhancing Aircraft Detection and Classification via Super-Resolution

## 📌 Overview

This project explores the application of Super-Resolution (SR) techniques to improve **military aircraft classification and detection** in low-resolution aerial imagery. Designed for a Computer Vision course, it showcases a full pipeline that integrates SR with deep learning models to increase accuracy in three distinct vision tasks.

**Project Title:** *From Blur to Precision: Improving Aircraft Classification and Detection via Super-Resolution*

**Team Members:**
- Emirhan Utku (2210765029)  
- Erdinç Arıcı (2210356035)  
- Gazi Kağan Soysal (2210356050)

---

## 🎯 Objective

The primary goal is to boost the performance of aircraft detection and classification models by enhancing the quality of aerial images using Super-Resolution techniques. This is critical in defense applications where images are often captured at low resolutions under complex conditions.

---

## 📂 Dataset

**Name:** [Military Aircraft Recognition Dataset](https://www.kaggle.com/datasets/khlaifiabilel/military-aircraft-recognition-dataset)

- 3,842 aerial images  
- 22,000+ annotated aircraft instances  
- 20 military aircraft classes  
- Horizontal and Oriented Bounding Box (OBB) annotations  
- Most images are 800×800 resolution

---

## 🧪 Methodology

The project follows a **three-stage pipeline** to evaluate the effect of SR on downstream tasks:

### ✅ Stage 1: Aircraft Classification  
- Cropped individual aircraft using bounding boxes  
- Compared classification with and without Super-Resolution  
- Model: MobileNetV2 with fine-tuned classification head

### 🎯 Stage 2: Object Detection (Horizontal Bounding Boxes)  
- Simulated low-res conditions via downsampling  
- Applied ESRGAN to enhance resolution  
- Detection with YOLOv8n trained on both versions

### 🔄 Stage 3: Oriented Object Detection (OBB)  
- Detected aircraft with orientation-specific bounding boxes  
- Used YOLOv8n-OBB trained on both original and SR-enhanced inputs

---

## 🧠 Technologies Used

- **Python, PyTorch** – Model development and training  
- **OpenCV** – Image preprocessing  
- **Ultralytics YOLOv8** – Detection models (horizontal + oriented)  
- **ESRGAN / EDSR** – Super-Resolution model (×4 upscaling)  
- **Google Colab** – GPU-accelerated training environment  

---

## 📊 Results Summary

| Stage | Baseline Accuracy | SR Accuracy | Improvement |
|-------|--------------------|-------------|-------------|
| **Classification** | ~70% | **92%+** | ✔️ Finer texture details improved accuracy |
| **Horizontal Detection** | mAP@0.5 ≈ 64% | **mAP@0.5 ≈ 96%** | ✔️ Better contour detection |
| **Oriented Detection** | Exact Match ≈ 34% | **≈ 56%** | ✔️ Improved angular precision |

Super-Resolution significantly improved performance in all stages by restoring high-frequency visual features, aiding detection and classification accuracy.

---

## 📈 Report and Documentation

Each stage is explained in detail in the [`VisionCourseProjectReport.pdf`](./Report.pdf), including:
- Preprocessing pipelines  
- Architecture setups  
- Training curves  
- Performance comparisons  
- Confusion matrices and visual results

The accompanying Jupyter Notebook (`VisionCourseProject.ipynb`) contains full implementation code with comments and visualizations.

---

## 🔍 Future Work

- Train domain-specific SR models focused on aircraft features  
- Introduce robustness to motion blur and sensor noise  
- Explore real-time integration and model compression for deployment

---

## 📄 Citation

If referencing this project in academic work:

> Utku, E., Arıcı, E., & Soysal, G. (2025). *From Blur to Precision: Improving Aircraft Classification and Detection via Super-Resolution*. ICLR 2025 (Conference Paper).

