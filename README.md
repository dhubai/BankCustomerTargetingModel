# Term Deposit Marketing Analysis

## Background
This project is developed for a startup specializing in machine learning solutions for the European banking sector. Focus areas include fraud detection, sentiment classification, and customer intention prediction. The primary objective is to create a machine learning system that analyzes call center data to enhance the success rate of product promotion calls, particularly focusing on term deposit subscriptions.

## Data Description
The dataset used for this project comes from a marketing campaign by a European bank, involving phone calls to customers regarding term deposit subscriptions. It encompasses various attributes like age, job, marital status, education, credit status, average yearly balance, and loan information. The key outcome variable is the customer's decision on the term deposit subscription.

## Analytical Process and Methodology

### Data Preparation and Exploration
- **Initial Steps**: Loading the dataset and generating summary statistics to understand the overall structure and attributes of the data.
- **Ensuring Data Quality**: Checking for missing values and duplicates to ensure the integrity and reliability of the data.
- **Exploratory Data Analysis**: Utilizing histograms and bar charts to explore the distributions of both numerical and categorical features.
- **Encoding Categorical Variables**: Transforming categorical data using OneHot and Label encoding, making it suitable for machine learning algorithms.

### Model Training and Evaluation
- **Model Selection and Training**: Training Decision Tree, Random Forest, and XGBoost models and evaluating their performance based on accuracy, ROC-AUC score, and classification reports.
- **Addressing Class Imbalance**: Employing SMOTE to balance the dataset and retraining the models to avoid biased predictions.
- **Adjusting Class Weights**: Increasing the weight of the minority class to further mitigate class imbalance.
- **Hyperparameter Tuning**: Using GridSearchCV and RandomizedSearchCV for fine-tuning the models' parameters.
- **Cross-Validation for Robustness**: Performing 5-fold cross-validation to ensure the models' robustness and generalizability.
- **Probability Threshold**: We utilized the predict_proba function in XGBoost to find the optimal probability threshold for maximizing the F1 score.

### Statistical Analysis
- **Significance Testing**: Conducting t-tests for numerical features and chi-square tests for categorical features to understand their influence on the target variable.

### Data Clustering and Feature Importance
- **Scaling and Clustering**: Applying K-Means clustering after scaling the data to identify distinct customer segments.
- **Feature Importance Analysis**: Using XGBoost to determine the most influential features for predicting term deposit subscriptions.

### Challenges and Solutions
- **Overcoming Class Imbalance**: Tackling class imbalance using SMOTE and class weight adjustments.
- **Model Selection and Optimization**: Experimenting with different models and optimizing them using cross-validation and grid search techniques.
- **Interpreting Complex Data**: Gaining valuable insights into the dataset through comprehensive EDA, statistical tests, and feature importance analysis.
- **Ensuring Model Generalizability**: Using cross-validation and a variety of models to build a model that generalizes well to unseen data.

### Conclusions
- **XGBoost's Superior Performance**: Highlighting XGBoost as the most effective model for this complex dataset.
- **Strategic Marketing Recommendations**: Recommending strategies based on the analysis, such as focusing on specific months, improving call quality, and targeting financially stable customers.
- **Targeted Marketing through Customer Segmentation**: Utilizing clustering results for more targeted and efficient marketing strategies.
---
