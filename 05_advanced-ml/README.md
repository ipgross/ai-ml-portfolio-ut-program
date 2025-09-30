# Project 5 — Advanced Machine Learning (Visa Application Prediction)

📌 **Personal / Academic project (outside of EA).**

---

## Overview
This project applies **advanced machine learning techniques** to predict whether a foreign worker visa application will be **Certified** or **Denied**.  

- **Business Problem:** Manual review of visa applications is time-consuming. We needed a scalable solution to prioritize likely approvals for faster processing.  
- **Goal:** Build an accurate, high-recall ML model that reduces missed approvals while maintaining strong F1 score.  
- **Key Skills:** Bagging, Boosting, Random Forests, Gradient Boosting, XGBoost, Hyperparameter Tuning, Class Imbalance Handling (SMOTE).  

---

## Contents
- [notebook.ipynb](./notebook.ipynb) → Colab notebook with data prep, model training, tuning, and evaluation  
- [slides.pdf](./slides.pdf) → project presentation (business problem, approach, results)  
- [data.csv](./data.csv) → visa application dataset  

---

## Data
- **Size:** ~32,000 historical visa applications (Office of Foreign Labor Certification – OFLC)  
- **Target:** `case_status` (Certified or Denied)  
- **Features:**  
  - `education_of_employee` — education level  
  - `has_job_experience` — prior job experience  
  - `requires_job_training` — training requirement  
  - `prevailing_wage` — offered wage  
  - `unit_of_wage` — Hourly, Monthly, Yearly, Weekly  
  - `full_time_position` — FT vs PT  
  - `region_of_employment`, `continent`  

---

## Models Tested
1. **Decision Tree** (baseline) → limited generalization  
2. **Bagging / Random Forest** → improved recall/F1  
3. **Boosting (AdaBoost, Gradient Boosting)** → stronger results  
4. **XGBoost (final model, tuned)** → best performance  

---

## Final Model (Tuned XGBoost)
- **Parameters:**  
  - `n_estimators=200`  
  - `learning_rate=0.1`  
  - `subsample=1.0`  
  - `gamma=5`  
- **Performance (Validation/Test):**  
  - F1 Score: ~83.7%  
  - Recall: ~89.2%  
  - Precision: ~78.9%  

---

## Insights
- Higher education levels (Bachelor’s, Master’s) → much higher approval rates  
- Prior job experience → strong positive factor  
- Full-time positions → more likely certified than part-time  
- Higher wages & yearly/monthly pay → higher certification likelihood  
- Hourly wage applicants less likely to be approved  

---

## Recommendations
- Use model to flag **likely approvals** for faster processing  
- Integrate into workflow as a **priority triage tool**  
- Retrain quarterly as new application data arrives  
- Add explainability (e.g., SHAP) to improve stakeholder trust  

---

## How to Explore
1. Open the notebook (`notebook.ipynb`) to see EDA, modeling, and evaluation  
2. Review `data.csv` for the dataset structure  
3. View `slides.pdf` for the executive summary  

---
