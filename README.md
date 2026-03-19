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
