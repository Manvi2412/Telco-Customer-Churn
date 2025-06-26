# Telco Customer Churn Prediction

This project predicts whether a telecom customer is likely to churn based on their service usage patterns and demographics. It includes data preprocessing, exploratory data analysis (EDA), machine learning modeling, and a deployed Streamlit web app for real-time prediction.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [EDA Insights](#eda-insights)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Streamlit Web App](#streamlit-web-app)
- [How to Run](#how-to-run)
- [Project Structure](#project-structure)
- [Future Improvements](#future-improvements)

## Project Overview

The goal is to help a telecom company identify customers at high risk of churn so that retention strategies can be implemented. The project includes:

- Data cleaning and feature engineering
- Handling class imbalance using SMOTE
- Building multiple classification models (Logistic Regression, Random Forest)
- Model evaluation using accuracy, precision, recall, F1-score, confusion matrix, and ROC-AUC
- A Streamlit app for user-friendly churn prediction

## Dataset

- **Source**: IBM Sample Dataset
- **File**: `Telco Customer Churn.csv`
- **Rows**: 7,043
- **Target Variable**: `Churn` (Yes/No)

## EDA Insights

- Customers with month-to-month contracts have the highest churn rate (~43%)
- Fiber optic internet users churn more than DSL users
- Churn is more likely when Online Security and Tech Support are not subscribed
- Electronic check users are more likely to churn than those using auto-payment
- Higher monthly charges are correlated with churn
- Longer tenure is associated with reduced churn

## Modeling

- Categorical variables encoded using one-hot encoding
- Final model: **Random Forest Classifier with class weights + SMOTE**
- Trained model saved as `telco_churn_model.pkl` for deployment

## Evaluation

- **Accuracy**: ~78%
- **Model performance** significantly improved with SMOTE and class weights
- ROC-AUC and confusion matrix were used for further evaluation

## Streamlit Web App

A Streamlit-based user interface allows users to:

- Input customer details
- Get churn prediction with probability
- Use a styled layout with sidebar and banner image

## How to Run

### Install dependencies

pip install -r requirements.txt

Run the Streamlit app
streamlit run app.py


telco-customer-churn-predictor/
├── app.py
├── telco_churn_model.pkl
├── Telco Customer Churn.csv
├── Telco_Customer_Churn_Report.docx
├── requirements.txt
└── README.md

Future Improvements
Deploy app online using Streamlit Cloud

Add SHAP explainability to the model

Connect to live customer data source or database

Improve feature engineering with behavioral metrics
