# Customer Churn Prediction & Retention Analytics

An end-to-end customer churn analytics project using Python, machine learning and Power BI to identify patterns associated with customer churn and translate analytical findings into customer-retention recommendations.

## Project Overview

Customer churn is an important business problem because identifying customers who may be more likely to leave can help organisations prioritise retention activity.

This project analyses a **synthetic dataset containing 100,000 customer records** to explore customer and account characteristics associated with churn and develop predictive classification models.

The project combines:

- Exploratory data analysis
- Data preparation and feature selection
- Logistic Regression
- XGBoost
- Hyperparameter tuning
- Model evaluation
- Power BI visualisation
- Business-focused recommendations

## Objectives

- Explore customer characteristics and patterns associated with churn.
- Identify customer segments with higher churn risk.
- Build and compare classification models.
- Evaluate model performance using accuracy, precision, recall and ROC-AUC.
- Tune the XGBoost model and examine the precision-recall trade-off.
- Translate analytical findings into practical customer-retention recommendations.
- Communicate findings through a Power BI dashboard.

## Tools & Technologies

- **Python**
- **Jupyter Notebook**
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **XGBoost**
- **Matplotlib**
- **Seaborn**
- **Power BI**

## Dataset

The project uses a synthetic customer churn dataset containing **100,000 records**.

Key variables include:

- Customer ID
- Age
- Gender
- Tenure
- Monthly charges
- Contract type
- Payment method
- Total charges
- Churn status

The analysis focuses on identifying patterns associated with customer churn.

## Analysis Approach

### 1. Exploratory Data Analysis

The dataset was explored to understand:

- Customer and account characteristics
- Overall churn distribution
- Relationships between customer attributes and churn
- Differences in churn patterns across customer segments
- Relationships between tenure, monthly charges and churn

The dataset contains approximately **33.14% churned customers**.

### 2. Data Preparation

The analysis included:

- Removing the customer identifier from modelling features
- Encoding categorical variables
- Preparing the churn target variable
- Removing missing observations
- Creating selected derived features for modelling
- Splitting the data into training and test sets

### 3. Feature Engineering

Additional features were created to explore customer risk patterns, including:

- `LogTotalCharges`
- `RiskIndex`
- `ExpensivePlan`

The `RiskIndex` combines shorter tenure and higher monthly charges to represent a simple customer-risk indicator.

### 4. Logistic Regression

Logistic Regression was used as a baseline classification model.

The model was trained using scaled features and class weighting to account for the class distribution.

**Results:**

- Accuracy: **69.1%**
- ROC-AUC: **0.773**

### 5. XGBoost

XGBoost was developed as a second classification model.

The baseline XGBoost model achieved:

- Accuracy: **75.7%**
- Precision for churn class: **66%**
- Recall for churn class: **55%**
- ROC-AUC: **0.802**

### 6. Hyperparameter Tuning

RandomizedSearchCV with **5-fold cross-validation** was used to explore XGBoost hyperparameters.

The search evaluated combinations of parameters including:

- Maximum tree depth
- Learning rate
- Number of estimators
- Subsampling
- Column sampling
- Minimum child weight
- Gamma
- Class weighting
- L1 and L2 regularisation

The search used an **F2 scoring metric**, placing greater emphasis on recall.

The tuned model achieved a ROC-AUC of approximately:

**0.808**

### 7. Classification Threshold

Rather than relying only on the default classification threshold, a threshold was selected using the precision-recall curve to balance precision and recall.

The selected threshold was approximately **0.693**.

At this threshold, the tuned XGBoost model achieved approximately:

- Accuracy: **76%**
- Precision: **63%**
- Recall: **61%**
- F1-score: **62%**
- ROC-AUC: **0.808**

## Model Comparison

| Model | Accuracy | ROC-AUC |
|---|---:|---:|
| Logistic Regression | 69.1% | 0.773 |
| XGBoost | 75.7% | 0.802 |
| Tuned XGBoost | ~76% | 0.808 |

The tuned XGBoost model produced the highest ROC-AUC among the evaluated models.

## Key Findings

The analysis identified several patterns associated with customer churn:

- Customers with **shorter tenure** showed higher churn risk.
- **Monthly charges** were higher on average among customers who churned.
- **Contract type** showed a meaningful relationship with churn, with month-to-month customers representing an important higher-risk segment.
- Longer-term contract types showed lower association with churn than month-to-month contracts.

These findings were used to identify customer segments that could be prioritised for retention activity.

## Business Recommendation

Based on the analysis, customers on **month-to-month contracts with shorter tenure** should be considered an important segment for targeted retention activity.

Potential actions could include:

- Early engagement with newer customers
- Targeted retention campaigns
- Offers or incentives for customers showing higher churn risk
- Monitoring customer segments using data-driven churn indicators

The objective is to help prioritise retention activity rather than applying the same approach to every customer.

## Power BI Dashboard

A Power BI dashboard was developed to communicate customer churn patterns, customer segments and model performance.

![Customer Churn Dashboard](dashboard/customer_churn_dashboard.png)

## Model Notebooks

### Logistic Regression

[View the Logistic Regression notebook](notebooks/logistic_regression.ipynb)

### XGBoost

[View the XGBoost notebook](notebooks/xgboost_model.ipynb)

## Skills Demonstrated

- Python data analysis
- Exploratory data analysis
- Data preparation
- Feature engineering
- Feature selection
- Classification modelling
- Logistic Regression
- XGBoost
- Hyperparameter tuning
- Cross-validation
- Model evaluation
- Precision-recall analysis
- Data visualisation
- Power BI
- Translating analytical findings into business recommendations

Conclusion

This project demonstrates an end-to-end approach to customer churn analytics, from exploring customer data and preparing features to developing and tuning predictive models, evaluating performance and translating findings into practical customer-retention recommendations.
