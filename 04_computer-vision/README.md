# Project 4 — Computer Vision (Safety Helmet Detection)

📌 **Personal / Academic project (outside of EA).**

---

## Overview
This project built an image classification system to detect **safety helmet usage** in industrial environments using **Convolutional Neural Networks (CNNs)** and **transfer learning (VGG-16)**.  

- **Goal:** Improve workplace safety by automatically detecting whether workers wear helmets  
- **Key Skills:** Computer Vision, CNNs, Transfer Learning, Data Augmentation, Model Evaluation  

---

## Contents
- [notebook.ipynb](./notebook.ipynb) → Colab notebook with model training & evaluation  
- [slides.pdf](./slides.pdf) → project presentation deck  
- [data_images.npy](./data_images.npy) → image dataset (200×200 RGB images)  
- [data_labels.csv](./data_labels.csv) → labels (helmet vs no helmet)  

---

## Data
- **Total Images:** 631  
  - 311 with helmets  
  - 320 without helmets  
- **Environments:** construction sites, factories, varied lighting/poses  
- **Preprocessing:** normalization, grayscale conversion, stratified splits (train/val/test)  

---

## Models Tested
1. **Basic CNN** — 3 Conv layers → Flatten → Dense → Output  
   - Val Recall: ~99%  

2. **VGG-16 (frozen base)**  
   - Val Recall: ~98%  

3. **VGG-16 + FFNN**  
   - Achieved perfect classification, more robust than baseline CNN  

4. **VGG-16 + FFNN + Data Augmentation**  
   - **Final model** — perfect classification with improved generalization  

---

## Results
- **Best Model:** VGG-16 + FFNN + Data Augmentation  
- **Performance:**  
  - Train Recall: 100%  
  - Validation Recall: 100%  
- Strong generalization across varied lighting, angles, and backgrounds  

---

## Business Takeaways
- Deploy model in **real-time camera systems** for workplace safety monitoring  
- Extend to detect other PPE (gloves, vests, eyewear)  
- Integrate with alert systems for immediate supervisor notifications  
- Retrain periodically with new image data to maintain robustness  

---

## How to Explore
1. Open the notebook (`notebook.ipynb`) for EDA, preprocessing, and model training  
2. Review `data_images.npy` and `data_labels.csv` for dataset samples  
3. Open the slides (`slides.pdf`) for a concise executive summary  

---
