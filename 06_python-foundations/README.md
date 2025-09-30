# Project 6 — Python Foundations (FoodHub Data Analysis)

📌 **Personal / Academic project (outside of EA).**

---

## Overview
This project demonstrates **data analysis and Python foundations** through an exploration of **FoodHub’s customer order data**.  
The goal was to analyze operational efficiency, customer satisfaction, and revenue drivers to provide actionable business recommendations.

- **Business Problem:** FoodHub needed insights to improve restaurant promotions, optimize delivery times, and enhance customer experience.  
- **Goal:** Use Python (pandas, numpy, matplotlib) for exploratory data analysis (EDA) and generate data-driven recommendations.  
- **Key Skills:** Python scripting, EDA, univariate/multivariate analysis, data visualization, and business insights.  

---

## Contents
- [notebook.ipynb](./notebook.ipynb) → Colab notebook with full analysis  
- [slides.pptx](./slides.pptx) → presentation deck (executive summary, findings, recommendations)  
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
- **Revenue Drivers:** Shake Shack was the top-performing restaurant by a large margin.  
- **Delivery Insights:** Weekend deliveries were faster (avg ~22 min) than weekdays (~28 min).  
- **Customer Satisfaction:** Low ratings correlated with longer prep and delivery times. High-cost orders were more likely to receive 5 stars.  
- **Cuisine Effects:** Some cuisines had longer prep times, which influenced ratings and order frequency.  

---

## Recommendations
- **Optimize Delivery Efficiency:** Add more drivers during weekday peaks.  
- **Customer Transparency:** Provide delivery time estimates upfront and consider a “Fast Delivery” badge for restaurants under 25 minutes.  
- **Promotions:** Prioritize high-rated restaurants with >50 reviews for campaigns.  
- **Revenue Strategy:** Use a tiered commission model (reduced rates for fast, high-rated restaurants) and encourage upselling with combo discounts.  

---

## How to Explore
1. Open the notebook (`notebook.ipynb`) for EDA and visualizations  
2. Revi
