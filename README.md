# Telco Customer Churn Prediction


## Project Overview

Customer churn is a major challenge for telecom companies, as losing customers directly impacts revenue.
In this project, I built and evaluated multiple machine learning models to Predict Whether a Customer will Churn or not, enabling businesses to take necessary retention actions.


## Objective

* Predict customer churn (Yes/No)
* Improve detection of high-risk customers
* Provide actionable insights for business decision-making


## Dataset

* Dataset: Telco Customer Churn Dataset
* Features include:

  * Customer demographics (gender, senior citizen, etc.)
  * Account information (tenure, contract type)
  * Services (internet, streaming, security)
  * Billing details (monthly & total charges)



## Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* ANN (Deep Learning)
* TensorFlow / Keras
* Matplotlib, Seaborn



## Models Used


### 🔹 XGBoost (Primary Model)

* Hyperparameter tuning using RandomizedSearchCV
* Best performing model

### 🔹 Artificial Neural Network (ANN)

* Fully connected neural network
* Used class weighting and dropout for improvement



## Model Performance


### XGBoost

* Accuracy: 83%
* ROC-AUC: 0.86
* Strong overall performance and class separation
  

### ANN

* Lower performance initially due to class imbalance
* Improved using:

  * Class weighting
  * Threshold tuning
* Improved Accuracy: 77%
* Improved ROC-AUC: 83%



## Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* Confusion Matrix
* Precision-Recall Curve



## Visualizations


### Confusion Matrix

* Shows correct vs incorrect predictions
* Helps identify false negatives (missed churners)
  

### ROC Curve

* Measures model’s ability to distinguish churners vs non-churners
* XGBoost achieved strong separation (~0.86 AUC)
  

### Precision-Recall Curve

* Highlights trade-off between:
  * Catching churners (recall)
  * Avoiding false alarms (precision)
    

### Feature Importance (XGBoost)

Top factors influencing churn:

* Contract type
* Tenure
* Monthly charges





## Challenges Faced




### 1. Imbalanced Dataset

* Majority of customers did not churn
* Models initially ignored churners

### 2. Data Preprocessing Issues

* Mixed data types (categorical + numerical)
* Missing values in `TotalCharges`

### 3. Encoding & Transformation Errors

* Sparse vs dense matrix issues
* Pandas vs NumPy compatibility problems

### 4. ANN Performance Issues

* Very low recall (~10%) initially
* Model biased toward non-churners




## Solutions Implemented

* Applied **OneHotEncoding with ColumnTransformer**
* Handled missing values using median imputation
* Used **class weighting** for ANN
* Applied **threshold tuning** to improve recall
* Performed **hyperparameter tuning** for XGBoost
* Ensured proper preprocessing pipeline




##  Business Value

This model provides real-world impact:



### Customer Retention

* Identifies customers likely to churn
* Enables proactive engagement strategies

### Cost Optimization

* Focus marketing efforts on high-risk customers
* Reduces unnecessary spending

### Strategic Insights

* Highlights key churn drivers
* Helps improve service offerings

### Decision Support

* Threshold tuning allows businesses to choose:

  * High recall → catch more churners
  * High precision → reduce false alarms



## Key Insights

* XGBoost outperformed ANN for structured/tabular data
* Precision-recall trade-off is critical in churn prediction
* Model performance depends heavily on:

  * Data preprocessing
  * Class imbalance handling
  * Threshold selection



## Author

Ahmed Farooq
Aspiring Machine Learning Engineer | Deep Learning | Generative AI

