# Project 2 — Neural Networks (Bank Churn Prediction)

📌 **Personal / Academic project (outside of EA).**

---

## Overview
Banks lose customers every month, and manual retention strategies aren’t scalable.  
This project builds a **neural network classifier** to predict which customers are most likely to churn in the next 6 months, allowing retention teams to intervene early.

- **Goal:** Predict churn risk with high recall so fewer high-risk customers are missed  
- **Key Skills:** Deep learning with TensorFlow/Keras, handling imbalanced data (SMOTE), regularization with Dropout, model tuning (SGD vs Adam)  

---

## Contents
- [notebook.ipynb](./notebook.ipynb) → Colab notebook with EDA, model building, and evaluation  
- [slides.pdf](./slides.pdf) → presentation summarizing business problem, approach, results  
- [data.csv](./data.csv) → dataset used for training/testing  

---

## Results
- Final model: **Neural Network with SMOTE + Adam + Dropout**  
- **Recall:** ~78%  
- **Precision:** ~46%  
- **F1 Score:** ~58%  
- **Accuracy:** ~77%  
- Key churn drivers: geography (Germany), inactivity, older age (45+), low product count  

---

## Business Takeaways
- Use the model to **flag at-risk customers** for proactive outreach (offers, support, incentives)  
- Retrain quarterly as new data arrives  
- Add explainability tools (e.g., SHAP) to provide retention teams with actionable insights  

---

## How to Explore
1. Open the notebook (`notebook.ipynb`) in Jupyter or Google Colab  
2. Review the dataset (`data.csv`)  
3. View the presentation (`slides.pdf`) for a business-focused summary  

---
