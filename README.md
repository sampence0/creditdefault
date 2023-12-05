# Home Credit Default Risk Analysis

## Project Overview
This project focuses on predicting the ability of potential borrowers to repay their loans, using the dataset from the [Home Credit Default Risk competition on Kaggle](https://www.kaggle.com/competitions/home-credit-default-risk/data). The goal is to assist in making informed loan decisions and in turn, ensure that clients capable of repayment are not rejected.

## Table of Contents
- [Background](#background)
- [Data Description](#data-description)
- [Methodology](#methodology)
- [Results](#results)

## Background
Credit plays a crucial role in the economy, and the ability to predict a borrower's repayment ability is vital to both the lender and the borrower. This project aims to make this prediction using various machine learning techniques, thus potentially enabling more clients to obtain loans and avoid the risk of unmanageable debt.

## Data Description
The dataset used in this project is from Home Credit, which consists of various features like loan annuities, client income, credit history, and more. The data is split into training and testing sets with multiple supplemental information in separate files.

## Methodology
- **Data Cleaning and Preprocessing**: Handling missing values, encoding categorical variables, and feature scaling.
- **Exploratory Data Analysis (EDA)**: Analyzing trends, patterns, and relationships in the data.
- **Feature Engineering**: Generating new features to improve model performance.
- **Model Training and Selection**: Implementing Random Forest and XGBoost models.
- **Evaluation**: Using metrics such as ROC AUC, precision, recall, and F1-score to evaluate model performance.

## Results

### Model Performance
- **Random Forest**: The Random Forest model achieved an ROC AUC score of 0.74. This performance indicates a fair level of predictive capability, particularly in balancing the trade-off between sensitivity and specificity in the imbalanced dataset.
- **XGBoost**: The XGBoost model outperformed the Random Forest with an ROC AUC score of 0.76, demonstrating its effectiveness in handling the complex relationships in the data and the class imbalance issue.

### Key Insights
- Feature importance analysis from both models highlighted the significance of specific variables in predicting loan repayment likelihood. However, further domain-specific feature engineering could potentially enhance model performance.
- The class imbalance in the dataset was a notable challenge. Various techniques, including resampling and adjusting class weights, were employed to mitigate its impact.

### Challenges and Solutions
- A key challenge was the substantial class imbalance within the dataset, which was addressed through class weighting and model-specific parameters like `scale_pos_weight` in XGBoost.
- The lack of extensive domain knowledge possibly limited the effectiveness of the feature engineering phase.

### Future Work
- Future improvements could include a more comprehensive approach to feature engineering, leveraging domain expertise to identify and construct more predictive features.
- Exploring alternative sampling techniques could further address the class imbalance issue, potentially improving model sensitivity to the minority class.
- Experimentation with different types of models, such as ensemble methods or advanced boosting algorithms, may yield improvements in predictive performance.

These results underscore the potential and challenges of using machine learning in credit risk assessment, offering a foundation for more informed and fair lending decisions.


