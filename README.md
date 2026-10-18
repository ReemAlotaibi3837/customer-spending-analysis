# Customer Spending Pattern Analysis

A data collection and preprocessing project in Python: assessing data quality, handling missing values and outliers, exploring spending behavior, and preparing the data for modeling.

Course project for *Data Collection and Preprocessing* (Umm Al-Qura University), completed as a pair with Lamar Alsubhi, May 2026.

## Overview

The analysis covers a retail dataset of 3,900 transactions and 18 columns and asks: **which features drive revenue?** The target variable is Purchase Amount (USD).

**Dataset:** *Customer Spending Patterns* by Ayesha Imran on Kaggle (it has since been removed). The file is not included in this repository.

## What the notebook covers

1. **Data quality assessment:** checks for missing values, duplicates, inconsistent labels, invalid values, and data types.
2. **Data cleaning:** The data was already clean, so missing-value handling was demonstrated on a 20% sample with 10% of three numerical columns removed on purpose. Mean and median imputation were compared, and mean imputation was chosen.
3. **Outlier detection:** boxplots, the IQR rule, and summary statistics. No outliers were found.
4. **Exploratory data analysis:** revenue by category, season, and gender, plus the effect of discounts, subscriptions, and purchase frequency.
5. **Transformation and feature engineering:** removing 13 irrelevant columns, MinMax scaling, one-hot encoding, and an Age Group feature.
6. **Feature selection and extraction:** correlation analysis, Recursive Feature Elimination (RFE) with Linear Regression, and PCA.

## Key findings

- The average purchase is about **$60** ($59.76) and stays stable across gender, season, discounts, subscriptions, and purchase frequency.
- **Revenue differences come from transaction volume, not price.** Clothing earns the most ($104,264) because it is bought most often (1,737 purchases).
- Male customers generate about twice the revenue of female customers because there are about twice as many of them (2,652 vs. 1,248). Average spend per purchase is nearly identical.
- Season, category, and the numerical features are all weak predictors of purchase amount (the highest correlation is about 0.04).

## Tools

Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn (MinMaxScaler, RFE, PCA)


## Limitations

The dataset appears to be synthetic: spending is evenly spread between $20 and $100 with no outliers, which real retail data rarely shows. Validate the findings on real-world data.

## Author

Reem Alotaibi
