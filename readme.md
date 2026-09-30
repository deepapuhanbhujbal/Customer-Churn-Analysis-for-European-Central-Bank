🏦 Customer Churn Analytics Dashboard
A Machine Learning–powered web application built using Python, Scikit-learn, and Streamlit to predict customer churn in European banking
system based on customer demographics,financial behaviour, and product utilization patterns

## Project Overview

- This project analyzes customer engagement,Product utilization,and churn behaviour using Machine Learning(XGBoost).
- The dashboard provides KPI insights, churn risk detection,and retention analysis.
- An interactive Streamlit dashboard was developed to visualize KPIs insights, predict churn risk detection and retention analysis.

## Objectives

- Identify high-risk churn customers
- Analyze product utilization impact
- Measure  customer retention strength
- Visualize feature importance
- Predict churn probability using Machine Learning


## Problem Statement

Customer churn directly impacts revenue and long-term profitability.
The goal of this project is to:

- Identify churn patterns
- Detect high-value at-risk customers
- Measure retention strength
- Build a predictive churn model

## Dataset Description

The dataset contains customer information from a European bank. The following features were used for analysis and model development:

Column                    Description
CreditScore	     -        Customer creditworthiness

Geography	     -        Customerlocation(France,Spain, Germany)

Gender	        -        Male / Female

Age              -        Customer Age

Tenure	        -        Number of Years with the bank

Balance	        -        Account balance

NumOfProducts	  -        Number of bank products

HasCrCard	     -        Credit card ownership

IsActiveMember	  -        Activity indicator

EstimatedSalary  -	       Estimated annual salary

Exited	        -        Churn indicator (target:1=churned,0=retained)


Dataset size    :10,000 customers
Features        : 13 variables
Target variable : Exited(Binary Classification)


## Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) was performed to understand customer behavior, engagement levels, and factors influencing churn.

Key analyses performed:

- Customer churn distribution analysis
- Churn rate comparison across different geographies
- Product utilization vs churn analysis
- Active vs inactive member churn comparison
- Balance distribution analysis for churned customers
- Customer age distribution analysis
- Correlation heatmap to identify relationships between variables

## Major Insights
Customers with low engagement and fewer banking products show higher churn probability, while active customers using multiple products demonstrate stronger retention.
## Feature Selection

Final features used for modeling:

- CreditScore  
- Geography  
- Gender  
- Age  
- Tenure  
- Balance  
- NumOfProducts  
- HasCrCard  
- IsActiveMember  
- EstimatedSalary  

Dropped:

- CustomerId  
- Surname


## Machine Learning Models Tested

Three classification models were implemented and compared:


|   Model              |    Accuracy     |    ROC-AUC      |
|----------------------|-----------------|-----------------|
|Logistic Regression   |  ~81%           |    ~0.78        |
|                      |                 |                 |
|Random Forest         |  ~84%           |    ~0.85        |
|                      |                 |                 |
|XGBoost               |  ~87%           |    ~0.87        |
|                      |                 |                 |


- final model selected : XGBoost
- Reason:
   - Higher accuracy
   - Better ROC-AUC curve
   - Improved recall for churn class
   - Strong feature importance interpretation

## Machine Learning Model Evaluation Metrics

- Model Used:XGBoost Classifier
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC curve
- Confusion Matrix
- Feature Importance

## Streamlit Dashboard Features

The interactive dashboard allows users to:

- Filter customers by geography
- Select age range
- Analyze churn distribution
- Detect high-value churn risks
- Analyze product utilization
- View model insights

## Key UI Features

- Interactive sidebar filters
- Geography selection
- Age range slider
- Active member filter
- KPI metrics display
- Customer churn distribution visualization
- Product utilization analysis
- High-value churn risk indicators
- Clean and responsive dashboard layout

## Project Workflow

1. Data Collection
2. Data Cleaning & Preprocessing
3. Exploratory Data Analysis
4. Feature Engineering
5. Model Training
6. Model Evaluation
7. Model Selection
8. Model Saving (Joblib)
9. Streamlit Dashboard Development
10. Deployment

## Tech Stack

- Python
- Streamlit
- Pandas
- Numpy
- Matplotlib &Seaborn
- Scikit-Learn
- XGBoost

## Project Structure

Customer_Churn_Analytics/ |

├── Streamlit_app_European_bank.py

├── Bank_analysis.ipynb

├── churn_model.pkl

├── best_model.pkl

├── European_Bank.csv

├── requirements.txt

└── README.md

## Results & Conclusion

- The XGBoost model achieved the best performance among the tested models.
- Inactive customers show higher churn probability compared to active members.
- Customers using fewer banking products are more likely to churn.
- Product utilization and customer engagement significantly influence churn behavior.
- The Streamlit dashboard enables interactive analysis and churn risk identification.

## Future Improvements

- Deploy the dashboard on cloud
- Add deep learning models
- Implement real-time churn prediction APIs
- Integrate advanced customer segmentation

## Author

Deepa Puhan Bhujbal

Developed using Python, Machine Learning and Streamlit
