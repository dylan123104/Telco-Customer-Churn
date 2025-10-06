# **Telco-Customer-Churn**

## **Project Overview**

* This project focuses on predicting customer churn for a telecommunications company using machine learning. The goal is to identify customers who are likely to leave the service, allowing the company to take proactive steps to retain them. By understanding the factors that drive churn, businesses can design more targeted retention strategies and improve overall customer satisfaction.

### **Objective**

* The primary objective of this analysis is to:

  * Predict whether a customer will churn based on their demographic and service usage data.

  * Understand which features are most influential in predicting churn.

  * Provide actionable insights for the business to reduce churn rates.

## **Dataset**

The dataset used in this project is the Telco Customer Churn dataset from Kaggle.
* It contains information on 7,043 customers, including:

  * Customer demographics (gender, senior citizen status, dependents, etc.)

  * Account information (contract type, payment method, tenure, monthly charges, etc.)

  * Service details (internet service, streaming services, tech support, and more)

  * Churn label (Yes/No)

## **Project Workflow**

### **Data Cleaning:**

* Removed missing or inconsistent values and standardized column formats.

* Converted categorical features into numerical form using one-hot encoding.

* Created two main DataFrames: one for exploration and one prepared for modeling.

### **Exploratory Data Analysis (EDA):**

* Examined distributions, customer segments, and churn patterns.

* Visualized churn by contract type, internet service, and payment method.

* Identified strong churn correlations with month-to-month contracts, electronic check payments, and fiber optic internet.

### **Feature Engineering:**

* Created binary and scaled variables for modeling.

* Checked for multicollinearity using VIF and retained only independent predictors.

### **Modeling:**

* Tested three models: Logistic Regression, Random Forest, and XGBoost.

* Logistic Regression performed the best with an accuracy of ~80% and ROC AUC of 0.83.

* Random Forest and XGBoost performed similarly but did not improve results significantly.

### **Model Optimization:**

* Applied class weighting and threshold tuning to improve recall on churners.

* Recall for churners increased from 0.55 to 0.82, allowing the model to identify the majority of customers likely to leave.

## **Key Insights**

* Customers with month-to-month contracts, electronic check payments, and fiber optic internet are at the highest risk of churn.

* Longer tenure and multi-year contracts are strong indicators of customer loyalty.

* Logistic Regression, when optimized, is both accurate and interpretable, making it ideal for business applications.

## **Business Impact**

* By deploying this model, the company can:

* Identify at-risk customers early.

* Target retention offers more effectively.

* Reduce churn-related revenue loss and improve long-term profitability.

* Periodically retrain the model with new data to maintain accuracy.

* Expand the analysis to include customer feedback and engagement metrics.
