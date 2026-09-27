# Customer Churn Prediction & Retention Analytics

An end-to-end customer churn analytics project using Python and machine learning to identify customers at higher risk of churn and translate analytical findings into actionable customer-retention recommendations.

## Project Overview

Customer churn is an important business problem because identifying customers who are likely to leave can help organisations develop targeted retention strategies.

This project analyses approximately **100,000 customer records** to explore patterns associated with customer churn and develop predictive classification models.

The analysis combines exploratory data analysis, feature selection, machine learning and model evaluation, with the findings translated into business recommendations and a Power BI dashboard.

## Objectives

* Explore customer characteristics and patterns associated with churn.
* Identify customer segments with higher churn risk.
* Build and compare classification models for churn prediction.
* Evaluate model performance using multiple classification metrics.
* Identify practical business actions that could support customer retention.
* Present key findings through a Power BI dashboard.

## Tools & Technologies

* **Python**
* **Jupyter Notebook**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **XGBoost**
* **Matplotlib**
* **Power BI**

## Dataset

The project uses approximately **100,000 customer records** containing customer and account-related variables, including:

* Contract type
* Customer tenure
* Monthly charges
* Other customer characteristics

The analysis focuses on identifying patterns and factors associated with customer churn.

## Analysis Process

### 1. Exploratory Data Analysis

The dataset was explored to understand:

* Customer and account characteristics
* Churn distribution
* Relationships between customer attributes and churn
* Differences in churn patterns across customer segments

### 2. Data Preparation

The data preparation process included:

* Reviewing the dataset structure and variables
* Preparing features for modelling
* Removing selected features that were not considered useful for the modelling process
* Preparing the data for classification models

### 3. Feature Selection

Feature selection was performed to remove selected variables and focus the modelling process on relevant information.

### 4. Model Development

Two classification models were developed and evaluated:

* **Logistic Regression**
* **XGBoost**

Hyperparameter tuning was performed for the models with the aim of balancing **precision and recall**.

## Model Performance

The models were evaluated using classification performance metrics including accuracy and ROC-AUC.

| Model               | Accuracy |  ROC-AUC |
| ------------------- | -------: | -------: |
| Logistic Regression |      69% |     0.77 |
| XGBoost             |      76% | **0.80** |

XGBoost produced stronger overall performance than the Logistic Regression model based on the evaluation results.

## Key Findings

The analysis identified several patterns associated with customer churn:

* Customers with **shorter tenure** showed higher churn risk.
* Customers on **monthly contracts** represented an important higher-risk segment.
* **Monthly charges** were associated with differences in churn behaviour.
* Some customer characteristics showed limited differentiation in churn patterns.

## Business Recommendation

Based on the analysis, customers on **monthly contracts with shorter tenure** should be considered a priority segment for targeted retention activity.

Potential retention strategies could include:

* Targeted retention campaigns
* Early-stage engagement with newer customers
* Incentives or offers designed for customers at higher risk of churn
* Monitoring customer segments using data-driven churn indicators

The objective is to use analytical insights to help prioritise retention activity rather than applying the same strategy to all customers.

## Power BI Dashboard

A Power BI dashboard was developed to communicate customer patterns and churn-related insights in an accessible format.

The dashboard supports exploration of customer characteristics and helps communicate findings to business stakeholders.

## Skills Demonstrated

This project demonstrates practical experience in:

* Data analysis with Python
* Exploratory data analysis
* Data preparation
* Feature selection
* Classification modelling
* Logistic Regression
* XGBoost
* Hyperparameter tuning
* Model evaluation
* Precision and recall analysis
* Data visualisation
* Power BI
* Translating analytical findings into business recommendations

## Conclusion

This project demonstrates an end-to-end approach to customer churn analytics, from exploring customer data and developing predictive models to identifying high-risk customer segments and translating findings into practical retention recommendations.

