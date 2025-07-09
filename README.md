# 📊 Financial-Fraud-Detection-Analysis
A machine learning-based solution for detecting fraudulent financial transactions, with an interactive Streamlit web application for real-time prediction.

## 🚀 Project Overview
Financial fraud causes billions in losses every year. This project explores a machine learning pipeline to detect fraudulent transactions using synthetic financial datasets. It includes exploratory data analysis, model training and evaluation, and an interactive web app built using Streamlit to predict fraud based on user input.

## 🔍 Features
Data preprocessing and feature engineering

Fraud detection using machine learning classifiers

Evaluation using precision, recall, F1-score

Streamlit web application for live prediction

Model serialized with joblib

# Dataset

The dataset used is AIML Dataset.csv, which contains the following columns:

step: Time step of the transaction.

type: Transaction type (e.g., PAYMENT, TRANSFER, CASH_OUT, DEPOSITS).

amount: Transaction amount.

nameOrig: Sender's account identifier.

oldbalanceOrg: Sender's balance before the transaction.

newbalanceOrig: Sender's balance after the transaction.

nameDest: Receiver's account identifier.

oldbalanceDest: Receiver's balance before the transaction.

newbalanceDest: Receiver's balance after the transaction.

isFraud: Binary label (1 for fraud, 0 for non-fraud).

isFlaggedFraud: Indicator for transactions flagged as potentially fraudulent.

The dataset contains 6,362,620 rows, with 8,213 fraudulent transactions and 6,354,407 non-fraudulent transactions, indicating a highly imbalanced dataset.


## 🧠 Model Training
All model training steps are included in the projcet_model.ipynb notebook:

Data loading & exploration

Feature selection

Model training and validation

Saving trained pipeline with joblib

Output: fraud_detection_pipeline.pkl
