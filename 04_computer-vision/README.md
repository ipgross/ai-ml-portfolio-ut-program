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
- [data_labels.csv](./data_labels.csv) → labels (helmet vs no helmet)  
- **Full image dataset (`data_images.npy`)** → [Download from Google Drive](https://drive.google.com/file/d/1MrEuAprqHQwQ_ELz1x-yxMTbuuSzSuP-/view?usp=drive_link)  

---

## Data
- **Total Images:** 631  
  - 311 with helmets  
  - 320 without helmets  
- **Preprocessing:** normalization, grayscale conversion, stratified splits (train/val/test)  

---

## Models Tested
1. **Basic CNN** — 3 Conv layers → Flatten → Dense → Output  
   - Val Recall: ~99%  

2. **VGG-16 (frozen base)**  
   - Val Recall: ~98%  

3. **VGG-16 + FFNN**  
   - Achieved robust classification  

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

---

## How to Explore
1. Open the notebook (`notebook.ipynb`) for preprocessing, model training, and results  
2. Review `data_labels.csv` for labels  
3. Download the full image dataset from [Google Drive](https://drive.google.com/file/d/1MrEuAprqHQwQ_ELz1x-yxMTbuuSzSuP-/view?usp=drive_link)  
4. Open the slides (`slides.pdf`) for a concise executive summary  

---
