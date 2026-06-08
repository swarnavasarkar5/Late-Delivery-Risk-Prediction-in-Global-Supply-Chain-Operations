# APL Logistics – Delivery Risk Intelligence Platform

## Overview

This project develops a Machine Learning-based Delivery Risk Intelligence Platform for predicting late deliveries in global supply chain operations. Using historical logistics, customer, product, and shipping data, the system identifies orders that are likely to be delayed before shipment, enabling proactive intervention and improved operational efficiency.

## Business Problem

Late deliveries result in SLA breaches, increased operational costs, customer dissatisfaction, and revenue loss. Traditional logistics reporting is reactive, identifying delays only after they occur. This project provides a predictive solution that helps operations teams prioritize high-risk orders and reduce delivery failures.

## Dataset

* **Records:** 180,519 Orders
* **Features:** 40 Original Variables
* **Target Variable:** `Late_delivery_risk` (Binary Classification)
* **Domain:** Supply Chain Analytics & Logistics

### Key Data Categories

* Customer Information
* Order Financials
* Shipping & Logistics
* Geography & Market Data
* Product Information
* Order Metadata

## Project Workflow

1. Data Cleaning & Preprocessing
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Categorical Encoding & SMOTE Balancing
5. Model Development
6. Cross-Validation & Model Selection
7. SHAP Explainability
8. Risk Scoring & Classification
9. Streamlit Dashboard Development

## Feature Engineering Highlights

Created domain-driven features such as:

* `tight_schedule_flag`
* `shipping_pressure`
* `express_shipping_flag`
* `shipping_mode_risk_score`
* `market_risk_score`
* `region_risk_score`
* `order_complexity`
* `high_value_order`

## Models Evaluated

| Model               | Accuracy   | F1 Score   | ROC-AUC    |
| ------------------- | ---------- | ---------- | ---------- |
| Logistic Regression | 0.6957     | 0.6650     | 0.7361     |
| Random Forest       | 0.7170     | 0.6848     | 0.7988     |
| XGBoost             | **0.7263** | **0.7058** | **0.8146** |

### Champion Model

**XGBoost Classifier**

* ROC-AUC: **0.8146**
* F1 Score: **0.7058**
* Best balance between Precision and Recall

## Explainable AI

SHAP (SHapley Additive Explanations) was used to interpret model predictions and identify the most influential factors driving delivery delays.

### Top Predictors

* Tight Schedule Flag
* Scheduled Shipping Days
* Shipping Mode
* Order Status
* Market Risk Score
* Discount Flag

## Risk Classification Framework

| Risk Level  | Probability Range |
| ----------- | ----------------- |
| Low Risk    | < 0.40            |
| Medium Risk | 0.40 – 0.70       |
| High Risk   | ≥ 0.70            |

The model identified **59,016 high-risk orders (32.7%)** requiring immediate operational attention.

## Streamlit Dashboard

Interactive dashboard with:

* Delivery Risk Overview
* Order-Level Prediction
* Regional & Shipping Mode Analysis
* Operations Action Panel
* Risk Filtering & Monitoring

## Technology Stack

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* SHAP
* Matplotlib
* Seaborn
* Streamlit
* Joblib

## Key Business Impact

* Predicts delivery delays before shipment
* Enables proactive risk management
* Prioritizes high-risk orders
* Reduces SLA violations
* Improves logistics planning and customer satisfaction
* Supports data-driven operational decision-making

## Future Enhancements

* Real-time API deployment
* Advanced time-series features
* NLP-based product analysis
* Cost-sensitive threshold optimization
* Multi-class delay prediction

---

**Author:** Swarnava Sarkar
**Domain:** Supply Chain Analytics | Machine Learning | Predictive Logistics
