# Project 6 — Python Foundations (FoodHub Data Analysis)

📌 **Personal / Academic project (outside of EA).**

---

## Overview
This project demonstrates **data analysis and Python foundations** through an exploration of **FoodHub’s customer order data**.  
The goal was to analyze operational efficiency, customer satisfaction, and revenue drivers to provide actionable business recommendations.

- **Business Problem:** FoodHub wanted insights to improve restaurant promotions, optimize delivery times, and enhance customer experience.  
- **Goal:** Use Python (pandas, numpy, matplotlib) for exploratory data analysis (EDA) and generate business recommendations.  
- **Key Skills:** Python scripting, EDA, univariate/multivariate analysis, data visualization, and insight generation.  

---

## Contents
- [notebook.ipynb](./notebook.ipynb) → Colab notebook with full analysis  
- [slides.pdf](./slides.pdf) → project presentation deck (executive summary, findings, recommendations)  
- [data.csv](./data.csv) → dataset (1,898 orders, 9 columns)  

---

## Data
- **Rows:** 1,898  
- **Columns:** 9  
- **Key Fields:**  
  - `restaurant_name`  
  - `cost_of_the_order`  
  - `food_preparation_time`  
  - `delivery_time`  
  - `rating`  
  - `cuisine_type`  
  - `day_of_the_week`  

---

## Key Findings
- **Revenue Distribution:** Shake Shack is a clear outlier, generating significantly higher revenue than other restaurants:contentReference[oaicite:0]{index=0}.  
- **Delivery Times:** Faster on weekends (~22 min) than weekdays (~28 min):contentReference[oaicite:1]{index=1}.  
- **Customer Satisfaction:** Lower ratings correlated with longer prep/delivery times; higher-cost orders were more likely to earn 5 stars:contentReference[oaicite:2]{index=2}.  
- **Cuisine Effects:** Certain cuisines had longer preparation times, impacting delivery efficiency and ratings:contentReference[oaicite:3]{index=3}.  

---

## Recommendations
- **Optimize Delivery Efficiency:** Add more drivers during weekday peaks:contentReference[oaicite:4]{index=4}.  
- **Customer Transparency:** Provide delivery time estimates upfront; introduce a “Fast Delivery” badge for restaurants with <25 min avg. delivery:contentReference[oaicite:5]{index=5}.  
- **Promotions:** Prioritize high-rated restaurants (>50 reviews) for campaigns:contentReference[oaicite:6]{index=6}.  
- **Revenue Strategy:** Encourage upselling with combo discounts on orders >$20; implement a tiered commission model:contentReference[oaicite:7]{index=7}.  

---

## How to Explore
1. Open the notebook (`notebook.ipynb`) for detailed EDA and visualizations  
2. Review the dataset (`data.csv`) for order-level data  
3. Open the slides (`slides.pdf`) for a concise business-focused summary  

---
