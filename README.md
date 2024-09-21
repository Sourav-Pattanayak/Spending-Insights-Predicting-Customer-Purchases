# Spending Insights – Predicting Customer Purchases 💳📊

### Table of Contents
1. [Introduction](#introduction) 📘
2. [Business Problem](#business-problem) 💼
3. [Dataset Overview](#dataset-overview) 📁
4. [Data Preprocessing](#data-preprocessing) 🧹
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda) 🔍
6. [Modeling](#modeling) 🤖
7. [Evaluation Metrics](#evaluation-metrics) 📏
8. [Results](#results) 🏆
9. [Conclusion](#conclusion) 🎯
10. [Dataset and Predictions](#dataset-and-predictions) 🗂️

---

## Introduction 📘
**FinPulse** is a growing financial services company providing banking solutions for both retail and corporate clients. One of its biggest challenges is understanding and predicting future customer spending habits, specifically focusing on **credit card (CC) spend**. Using machine learning models, FinPulse aims to optimize customer engagement and predict potential revenue based on historical data.

This project focuses on predicting **Future Credit Card Spend** using customer demographic and transaction data, ultimately helping the company drive more targeted financial services.

## Business Problem 💼
FinPulse’s marketing team wants to identify which clients are likely to spend the most on their credit cards in the upcoming months. Accurate predictions will help FinPulse:
- **🎯 Target high-spending clients** for marketing campaigns.
- **📈 Optimize credit allocation** based on future spending behavior.
- **💰 Predict potential revenue growth** from customer transactions.
- **🚨 Reduce financial risk** by identifying customers who may require credit limit adjustments.

## Dataset Overview 📁
The dataset consists of three main tables:
1. **Client Information (`ClientInfo.csv`)**: Includes client demographics such as age, gender, and years with the bank.
2. **Client Transactions (`ClientTransactions.csv`)**: Monthly transaction data, including debit and credit spend details.
3. **Financial Forecast (`FinancialForecast.csv`)**: Data about active loans, loan inquiries, and EMI payments.

📂 **Dataset**: [Download Here](https://drive.google.com/drive/folders/1Ze1-BYjuDUiwAiF-y1P5MY-rCxNKdxFA?usp=sharing).

Key columns include:
- `Client_ID`: Unique identifier for each customer.
- `Years_of_Age`: Customer’s age.
- `Earnings`: Client income category (Above Average, Average, Below Average).
- `Has_Personal_Loan`, `Has_Vehicle_Loan`: Indicators for active loans.
- `Future_CC_Spend`: **Target Variable** – Future predicted credit card spend.

## Data Preprocessing 🧹
- **Data Cleaning**: Missing values in the target column (`Future_CC_Spend`) were handled through prediction, while unnecessary columns were removed.
- **Categorical Encoding**: One-hot encoding was applied to categorical variables like `Earnings`, `Sex`, and `Account_Category`.
- **Feature Selection**: Features that had low correlation with the target variable were dropped to enhance model performance.

## Exploratory Data Analysis (EDA) 🔍
Key insights from the EDA:
- **Income vs Spend**: Customers with higher income (`Earnings` = Above Average) tend to spend more on credit cards.
- **Banking Tenure**: Clients with longer relationships with the bank are more likely to increase their spending.
- **Loan Impact**: Clients with active loans, particularly those with high EMI payments, show lower credit card spending due to financial obligations.

Visualizations, such as correlation matrices and scatter plots, were used to identify important patterns in the data. 📊

## Modeling 🤖
The goal is to predict **Future Credit Card Spend** (a continuous variable), so regression models were applied. Here's the process:
1. **Model Selection**: A **Random Forest Regressor** was chosen due to its ability to handle large datasets and complex relationships while reducing overfitting.
2. **Training & Testing**: The data was split into training and testing sets, where the test set contained rows with missing `Future_CC_Spend`.
3. **Model Training**: The model was trained using customer demographics, transaction data, and financial behavior.

## Evaluation Metrics 📏
The following metrics were used to evaluate the performance of the model:
- **R² Score**: 0.85 – Meaning the model explained 85% of the variance in the target variable.
- **Mean Absolute Error (MAE)**: 1238.98 units – Indicating the average difference between the actual and predicted values.
- **Root Mean Squared Error (RMSE)**: 1430.70 – Reflects the magnitude of the prediction errors.
- **RMSPE**: 153.80% – Points to significant errors caused by data outliers or potential model improvement needs.

## Results 🏆
Here are the key outcomes from the model:
1. **High-Spending Customers Identified**: The model successfully predicted clients with future high credit card spends, which helps the marketing team focus on those clients.
2. **Loan Impact on Spend**: Clients with high EMI payments show significantly lower future spending, allowing the bank to adjust its credit allocation strategies.
3. **High Credit Spend Predictors**: Income, transaction gaps, and job tenure were identified as strong predictors of future credit card spending behavior.

You can download the predicted credit card spend values from [this link](https://drive.google.com/drive/folders/172juUsqkqiHQs2i1lmQXGSEwsUS7H-hl?usp=sharing).

### Additional Insights:
- **Marketing Strategies**: High-income clients and those with long relationships with the bank could be targeted with premium credit offers.
- **Credit Risk Mitigation**: Customers with heavy loans and EMIs could be flagged for credit limit adjustments to avoid defaults.
- **Revenue Forecasting**: The model’s accuracy helps forecast potential revenue streams based on predicted spending behavior.

## Conclusion 🎯
This project demonstrated the effective use of machine learning to predict customer spending behavior. By accurately predicting **Future Credit Card Spend**, FinPulse can:
- **Enhance marketing campaigns** by targeting high spenders.
- **Optimize risk management** by adjusting credit limits for high-risk customers.
- **Improve revenue predictions**, helping the company better plan its financial strategies.

While the model performed well, there is room for improvement, especially with **RMSPE**. Additional **feature engineering** and **hyperparameter tuning** can further reduce errors and boost prediction accuracy.

## Dataset and Predictions 🗂️
- **📂 Dataset**: [Download Here](https://drive.google.com/drive/folders/1Ze1-BYjuDUiwAiF-y1P5MY-rCxNKdxFA?usp=sharing).
- **📊 Predicted Credit Card Spend**: [Download CSV Here](https://drive.google.com/drive/folders/172juUsqkqiHQs2i1lmQXGSEwsUS7H-hl?usp=sharing).

---

### Let me know if you'd like further adjustments or additional sections!
