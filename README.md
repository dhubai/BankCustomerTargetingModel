# Bank Customer Targeting Model
### Optimizing Marketing Strategies with Predictive Analytics

## Project Overview

This project aims to develop a robust machine learning model to predict customer subscriptions to term deposits using call center data from a European banking institution. The goal is to enhance the success rate of marketing calls by identifying which customers are more likely to subscribe to the bank's investment products. This solution will help the bank prioritize customers for follow-up calls, optimize marketing strategies, and ultimately improve campaign performance.

## Data Description

The dataset used for this project is derived from direct marketing efforts of a European bank. The data includes information about customers' demographic characteristics, past interactions with the bank, and outcomes of previous marketing campaigns. Key attributes include:

- **Age**: Age of the customer.
- **Job**: Type of job.
- **Marital**: Marital status.
- **Education**: Education level.
- **Default**: Whether the customer has a credit in default.
- **Balance**: Average yearly balance in euros.
- **Housing**: Whether the customer has a housing loan.
- **Loan**: Whether the customer has a personal loan.
- **Contact**: Contact communication type.
- **Duration**: Duration of the last contact in seconds.
- **Campaign**: Number of contacts during the current campaign.

**Target Variable:**
- **Y**: Whether the client subscribed to a term deposit (Yes/No).


## Project Goals

- **Primary Goal**: Predict whether a customer will subscribe to a term deposit (Yes/No).
- **Success Metric**: Achieve an accuracy score of 81% or above using 5-fold cross-validation.
- **Secondary Goals**:
  - Identify customer segments most likely to subscribe.
  - Determine which features most significantly influence the likelihood of subscription.

## Models and Algorithms Used

The following machine learning models and algorithms were employed to achieve the project's objectives:

1. **Decision Tree Classifier**: A tree-based model that splits data into branches to make predictions based on feature values.
2. **Random Forest Classifier**: An ensemble method that builds multiple decision trees and merges them to improve prediction accuracy and control overfitting.
3. **XGBoost Classifier**: An optimized gradient boosting algorithm that builds trees sequentially to reduce errors and improve performance.
4. **Synthetic Minority Over-sampling Technique (SMOTE)**: A method for handling class imbalance by generating synthetic samples for the minority class.
5. **K-Means Clustering**: An unsupervised learning algorithm used to segment customers into distinct groups based on their attributes.
6. **Statistical Tests (T-tests and Chi-square tests)**: Statistical methods used to identify significant numerical and categorical features that impact customer decisions.

## Methodology

1. **Data Preprocessing**: 
   - Handled missing values, encoded categorical variables, and scaled numerical features.
2. **Exploratory Data Analysis (EDA)**:
   - Conducted statistical tests (T-tests, Chi-square) to identify significant features.
   - Visualized feature distributions and correlations.
3. **Modeling**:
   - Trained and evaluated multiple machine learning models (Decision Tree, Random Forest, XGBoost).
   - Performed hyperparameter tuning using GridSearchCV and RandomizedSearchCV.
   - Applied SMOTE to handle class imbalance.
4. **Feature Importance and Segmentation**:
   - Leveraged XGBoost for feature importance analysis.
   - Applied K-Means clustering to identify customer segments for targeted marketing.

## Results

- **Model Performance**:
  - **Decision Tree**: Accuracy = 91.79%, ROC-AUC = 0.6791
  - **Random Forest**: Accuracy = 93.25%, ROC-AUC = 0.6010
  - **XGBoost**: Accuracy = 92.21%, ROC-AUC = 0.8141 (Best Model)

- **Key Insights**:
  - **XGBoost** outperformed other models in distinguishing between classes, particularly due to its superior ROC-AUC and F1 scores.
  - **Optimal Threshold**: A threshold of 0.58 for the XGBoost model maximized the F1 score to 0.5751.

- **Statistical Analysis**:
  - Significant predictors include **Age**, **Balance**, **Duration of Call**, **Job Type**, **Marital Status**, **Education**, **Housing Loan**, and **Contact Method**.

## Insights and Recommendations

- **Target Segments**:
  - **Cluster 1**: High engagement customers with lower balances, typically contacted early in the month.
  - **Cluster 2**: Customers with high balances and moderate engagement, contacted later in the month.

- **Marketing Strategy**:
  - Focus efforts on Cluster 1 for their engagement and Cluster 2 for their financial readiness to invest.
  - Align marketing campaigns with key months (March, August, July) to optimize customer reach.
  - Emphasize call quality and length, as longer calls positively impact subscription rates.

## Future Work

- Incorporate additional data sources (e.g., online behavior, customer feedback).
- Explore more advanced ensemble techniques or deep learning models.
- Develop a real-time scoring system to prioritize customer calls dynamically.
