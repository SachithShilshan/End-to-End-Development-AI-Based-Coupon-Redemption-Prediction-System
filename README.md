# End-to-End-Development-AI-Based-Coupon-Redemption-Prediction-System

## Overview

● Predict binary outcome redemption_status (1 = Redeemed, 0 = Not Redeemed)

● Provide interpretable and accurate results

● Deploy model to Azure Web App for API access

● Integrate predictions into Power BI For visualization


## Architecture (End to End )

1. Data Sources - Kaggle Dataset
2. Use Colab
   
    ● Data Preprocessing

    ● Feature Engineering

    ● Train the Models:

       o Logistic Regression
       o Decision Tree
       o XGBoost (with PCA)

    ● Save Models (joblib / JSON)
4. GitHub (use for version control)
5. Deploy API on Azure Web App (Flask + Uvicorn + Gunicorn )
6. Power BI - Visualization
- Power Query M - Sends JSON POST request then Receives Prediction

## Feature Engineering

We calculaye below Feature

o Campaign -campaign_type, campaign_duration

o Coupon Mapping -coupon_item_count, unique_brands, unique_categories

o Transactions -total_qty, avg_qty, avg_price, avg_coupon_disc

o Customer -age_range, family_size, marital_status, rented, income_bracket

o Purchase History -purchased_coupon_item_before

And also PCA
- PC1 to PC7

## Model Training Summary

    o Logistic Regression Accuracy ~84%
    o Decision Tree Accuracy ~75%
    o XGBoost + PCA Accuracy ~ 99 %
  
GitHub
Repo: https://github.com/SachithShilshan/coupon-api

● Use for Version control for code ,models and auto-deploy to Azure App Service

## Deployment (Azure Web App)

● Models saved using joblib

● Flask app exposes 3 endpoints:

o /predict_lr – Logistic Regression - https://coupon-api4-hhbqh9f9c8azhud9.canadacentral-01.azurewebsites.net/predict

o /predict_dt – Decision Tree -https://coupon-api4-hhbqh9f9c8azhud9.canadacentral-01.azurewebsites.net/predict_dt

o /predict_xg – XGBoost + PCA - https://coupon-api4-hhbqh9f9c8azhud9.canadacentral-01.azurewebsites.net/predict_xg

● Hosted on Azure Web App Service

● API tested via Python requests and Power BI

## Power BI Integration

● Power Query used to data transformation:

o Data Transformation

o Send each record to Azure API

o Parse prediction and probability

● Predictions visualized with:

o Bar charts for redemption
o Tables with customer/campaign details…
o Filters like category,Age…

For that I make draft visualization

![image](https://github.com/user-attachments/assets/72040657-dccc-412d-a74a-de185aba9ce2)

We can create Excel or other for user to enter data then it loads to power bi and make
predictions .So,finally data visualize in power bi dashboard.

Finaly, This solution combines with robust machine learning with cloud deployment and
BI integration. It allows business teams to make data-driven decisions in real-time
and optimize marketing outcomes.

## Appendices

● Colab Notbook
https://drive.google.com/file/d/1V5jZB5EivT8xR1FU0DrfzlH66nVtkXm4/view?usp=sharing

● GitHub Repo
https://github.com/SachithShilshan/coupon-api

● API URLs

   o Logistic Regression
     https://coupon-api4-hhbqh9f9c8azhud9.canadacentral-01.azurewebsites.net/predict

   o Decision Tree
     https://coupon-api4-hhbqh9f9c8azhud9.canadacentral-01.azurewebsites.net/predict_dt

   o XGBoost
     https://coupon-api4-hhbqh9f9c8azhud9.canadacentral-01.azurewebsites.net/predict_xg

● Power BI dashboard file
https://drive.google.com/file/d/1Ms03DXKZZok07hUFUHq3573iABM3oJSe/view?usp=sharing

