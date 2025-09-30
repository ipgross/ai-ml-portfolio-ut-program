# Project 7 — Model Deployment: SuperKart Sales Forecast

📌 **Capstone Project — UT Austin AI/ML Program**  
📌 **Personal / Academic project (outside of EA).**

---

## Overview
This capstone project demonstrates an **end-to-end ML system**: from data ingestion to model deployment with a live frontend + backend.  
The goal was to build a **sales forecasting model** for a retail chain (**SuperKart**) that predicts product-level sales per store, enabling better inventory planning and reducing stockouts/overstocking.

- **Business Problem:** Manual forecasts were inaccurate, leading to wastage and missed sales:contentReference[oaicite:0]{index=0}.  
- **Solution:** Train a high-performance ML model, deploy it via API, and make it accessible through a user-friendly web app:contentReference[oaicite:1]{index=1}.  

---

## Live Demo
- **Frontend (Streamlit UI):** [Try it here](https://huggingface.co/spaces/igross/superkart-sales-forecast-frontend-space)  
- **Backend API (Flask + Docker):** [View API](https://huggingface.co/spaces/igross/superkart-sales-forecast-backend)  

---

## Contents
- [notebook.ipynb](./notebook.ipynb) → Colab notebook (EDA → model → tuning → evaluation)  
- [slides.pdf](./slides.pdf) → project presentation deck  
- [data.csv](./data.csv) → dataset used for modeling  
- API & frontend deployment on Hugging Face Spaces  

---

## Data
- **Rows:** ~8,500 product–store records  
- **Features:** product attributes, store characteristics, pricing info:contentReference[oaicite:2]{index=2}  
- **Target:** total product–store sales (continuous variable)  

Key fields:  
- `Product_Weight` (kg)  
- `Product_Sugar_Content` (Low, Regular, None)  
- `Product_Allocated_Area` (shelf space)  
- `Product_MRP` (price)  
- `Store_Size`, `Store_Type`, `Store_Location_City_Type`  
- `Store_Age_Years`  
- `Product_Type_Category` (Perishable vs Non-Perishable):contentReference[oaicite:3]{index=3}  

---

## Modeling
- **Algorithm:** XGBoost Regressor (chosen for tabular data robustness):contentReference[oaicite:4]{index=4}  
- **Pipeline:** scikit-learn `ColumnTransformer` + preprocessing (scaling, encoding) integrated with XGBoost:contentReference[oaicite:5]{index=5}  
- **Hyperparameter Tuning:** GridSearchCV with 5-fold CV optimized depth, learning rate, estimators, subsampling:contentReference[oaicite:6]{index=6}  

**Performance:**  
- Training R²: ~0.94  
- Test R²: ~0.92  
- RMSE: ~300 sales units:contentReference[oaicite:7]{index=7}  

---

## Deployment
- **Backend:** Flask API (`/v1/predict` endpoint), containerized with Docker, deployed on Hugging Face Spaces:contentReference[oaicite:8]{index=8}  
- **Frontend:** Streamlit app with dropdowns/inputs → sends JSON to API → displays predictions:contentReference[oaicite:9]{index=9}  
- **Artifacts:** model serialized with `joblib` for reproducible serving  

---

## Results & Insights
- Pricing (MRP) and shelf allocation strongly influence sales:contentReference[oaicite:10]{index=10}  
- Tier 2 cities outperform Tier 1 & 3 in total sales:contentReference[oaicite:11]{index=11}  
- Perishable items show seasonality and higher sensitivity to pricing:contentReference[oaicite:12]{index=12}  
- Final model achieved **high accuracy, low error, and robust generalization**:contentReference[oaicite:13]{index=13}  

---

## Business Recommendations
1. Deploy the model across stores to support SKU-level demand forecasting:contentReference[oaicite:14]{index=14}  
2. Integrate with ERP systems to auto-trigger purchase orders:contentReference[oaicite:15]{index=15}  
3. Retrain quarterly to adapt to evolving sales patterns:contentReference[oaicite:16]{index=16}  
4. Expand dataset with promotions & seasonality for improved accuracy:contentReference[oaicite:17]{index=17}  
5. Enhance frontend dashboards with trend analysis in addition to point forecasts:contentReference[oaicite:18]{index=18}  

---

## Analytics Engineering Highlights
This capstone ties ML to **analytics engineering best practices**:  
- **Pipelines:** reproducible preprocessing pipeline with `ColumnTransformer` ensures training–serving consistency  
- **Reproducibility:** hyperparameter tuning + joblib model artifacts allow redeployment with versioning  
- **Deployment Engineering:** containerized API + frontend separation mirrors modern production MLOps stacks  
- **Data Integration:** project designed for ERP integration, showing applied analytics engineering mindset:contentReference[oaicite:19]{index=19}  

---

## How to Explore
1. Launch the [frontend app](https://huggingface.co/spaces/igross/superkart-sales-forecast-frontend-space) and test product/store inputs  
2. Call the [backend API](https://huggingface.co/spaces/igross/superkart-sales-forecast-backend) with a JSON payload  
3. Review the notebook (`notebook.ipynb`) for EDA, model training, and tuning  
4. Open `slides.pdf` for the executive presentation  

---
