# 🛒 E-Commerce Customer Churn Prediction & RFM Analysis

## 📌 Project Overview
In the highly competitive e-commerce sector, retaining existing customers is significantly more cost-effective than acquiring new ones. This project aims to identify customers who are likely to churn (stop purchasing) using machine learning techniques based on their historical transaction data.

## 🎯 Business Problem
The primary goal is to predict customer churn accurately so that targeted marketing campaigns (e.g., special discounts, retention emails) can be applied to at-risk customers, ultimately maximizing Customer Lifetime Value (CLV).

## 🛠️ Methodology & Tech Stack
* **Language/Libraries:** Python, Pandas, Scikit-learn, Imbalanced-learn (SMOTE), Seaborn.
* **Feature Engineering:** Extracted **RFM** (Recency, Frequency, Monetary) metrics and Average Order Value (AOV) from raw invoice data.
* **Data Leakage Prevention:** Excluded the 'Recency' feature during model training, as it was used to define the Churn target variable (Rule: Recency > 180 days = Churn).
* **Handling Imbalanced Data:** Applied **SMOTE** (Synthetic Minority Over-sampling Technique) to the training set to address the highly imbalanced nature of churn data.
* **Modeling:** Trained a **Random Forest Classifier**.

## 📊 Results & Business Impact
In this business context, missing a churning customer (False Negative) is much more costly than sending a discount to a loyal customer (False Positive). Therefore, the model was optimized for **Recall**.
* **Baseline Model Recall:** 38%
* **Optimized Model (with SMOTE + AOV) Recall:** 56%
* **Conclusion:** By engineering new features and addressing class imbalance, the model's ability to catch churning customers increased by nearly 50%, providing a strong baseline for proactive retention strategies.# E-Commerce-Churn-Prediction

## 📈 Interactive Power BI Dashboard

To translate the model's output into a decision-support tool for retention teams, the churn predictions were visualized in an interactive Power BI dashboard.

Dashboard highlights:

KPI overview: total customer count, overall churn rate, and the model's recall improvement (38% → 56%) at a glance.
Segment-level view: customers grouped into RFM-based segments (Champions, Loyal Customers, At Risk, Lost, New/Occasional), sized by customer count and positioned by average recency and spend.
Churn breakdown by segment: bar chart showing churned vs. retained customers within each segment.
Filterable risk table: a sortable, slicer-driven table listing customers by churn risk score, filterable by segment and country — allowing a retention team to act directly on the highest-risk accounts.

📁 churn_risk.pbix — open in Power BI Desktop to explore interactively.

<img width="1812" height="831" alt="Ekran görüntüsü 2026-07-26 155557" src="https://github.com/user-attachments/assets/22e2bd74-3780-4491-9aec-ee408479ecbe" />

Tech used for the dashboard: Power BI, DAX (custom measures for churn rate, average risk score, and customer counts).
