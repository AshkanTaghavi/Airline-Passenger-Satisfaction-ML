# Airline Passenger Satisfaction Analysis

**Author:** Ashkan Taghavi  
**Project:** Midterm - Take Home Exam

## Overview

This project aims to predict airline passenger satisfaction and identify key factors associated with it using a dataset from a satisfaction survey.

## Questions of Interest

1. Can you predict passenger satisfaction?
2. What factors are associated with passenger satisfaction?

## Data Preparation and Preprocessing

1. **Load Packages and Data:** 
    - Packages: pandas, numpy, matplotlib, seaborn, xgboost, sklearn, imblearn
    - Data: Two datasets merged into one (129,880 rows × 24 columns)

2. **Cleaning Data:**
    - Dropped 393 rows with missing values in 'Arrival Delay in Minutes'
    - Created a new 'Total Delay' column combining 'Arrival Delay in Minutes' and 'Departure Delay in Minutes'
    - Checked class balance: 73,225 'neutral or dissatisfied' vs. 56,262 'satisfied'

## Exploratory Data Analysis (EDA)

- Summary statistics and visualizations to understand data distributions and relationships
- Key observations on gender, customer type, type of travel, class, age, and flight distance
- Correlation analysis to identify significant relationships

## Modeling

1. **Data Preparation:**
    - Used ColumnTransformer and Pipelines for preprocessing
    - Applied various classifiers: Naive Bayes, XGBoost, Random Forest, and Neural Networks

2. **Model Performance:**
    - Naive Bayes: Best F1 Score (Bernoulli): 0.8403, Accuracy: 0.8649
    - XGBoost: F1 Score: 0.9504, Accuracy: 0.9576
    - Random Forest: F1 Score: 0.9563, Accuracy: 0.9626 (Best Model)
    - Neural Networks: F1 Score: 0.9544, Accuracy: 0.9610

## Key Factors Influencing Satisfaction

- **Positive Influence:** Business travel, loyal customers, Business class, on-board service, online boarding, inflight wifi service
- **Negative Influence:** Personal travel, disloyal customers, Eco class, total delay, younger ages

## Recommendations

- Enhance loyalty programs and services for business travelers
- Invest in better inflight services, especially in Economy class
- Implement randomized sampling for future surveys to avoid bias

## Conclusion

The Random Forest model was the best performer, demonstrating high prediction accuracy for passenger satisfaction. Key factors like travel class, type of travel, and inflight services significantly influence satisfaction levels.
