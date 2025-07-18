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


## Analysis and Methodology
The analysis was conducted in several steps:

Data Loading and Initial Inspection: Loaded the dataset into a pandas DataFrame and performed initial checks on its shape, data types, and missing values.

## Exploratory Data Analysis (EDA):

Analyzed the distribution of transaction types.

Investigated the frequency of fraudulent transactions and flagged fraudulent transactions.

Examined the distribution of transaction amounts.

Visualized the relationship between transaction type and fraud rate.

Analyzed the distribution of transaction amounts, including using a log scale due to the wide range of values.

Visualized the relationship between transaction amount and fraud for amounts under 50k.

![image](https://github.com/user-attachments/assets/52de99e7-dca3-4b6d-b259-29d1a79b260c)

![image](https://github.com/user-attachments/assets/d2940775-2805-4c21-97ae-e8921d040990)


![image](https://github.com/user-attachments/assets/67904ef5-3189-4b9e-9b10-f70489df97fc)


## Feature Engineering:

Created new features newbalancDiffeOrig and newbalancDiffeDest to represent the change in balance for the origin and destination accounts, respectively.

## Data Preprocessing:

Dropped irrelevant columns (nameOrig, nameDest, isFlaggedFraud).

Separated the target variable (isFraud) from the features.

Split the data into training and testing sets using stratification to maintain the proportion of fraudulent transactions.

Applied one-hot encoding to the categorical feature (type).

Scaled the numerical features using StandardScaler.

## Model Training:

Used a Logistic Regression model with class_weight="balanced" to address the class imbalance issue.
Trained the model on the preprocessed training data.

## Model Evaluation:
Evaluated the model's performance on the test set using a classification report, confusion matrix, and accuracy score.

## Model Saving:

Saved the trained pipeline to a file named fraud_detection_pipeline.pkl for future use.

## Results
The Logistic Regression model achieved an accuracy of approximately 94.88%. The classification report shows the precision, recall, and f1-score for both fraudulent and non-fraudulent classes, highlighting the model's performance in identifying fraudulent transactions despite the dataset's imbalance.

The confusion matrix provides a detailed breakdown of true positives, true negatives, false positives, and false negatives.

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/d6d959dc-12f0-42f3-8430-948dba38a52f" />

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/c3626018-6a0d-43c0-8845-35f02d13de20" />

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/abdc0e83-282d-47bb-900b-cc5eca8cf87a" />

