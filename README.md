# Titanic-data-analysis
# Titanic Survival Prediction

## Purpose
Develop a machine learning model to predict the survival of Titanic passengers based on their demographic and travel-related features.

## Project Overview
This repository contains a comprehensive analysis and model development pipeline for predicting Titanic survival. The project covers exploratory data analysis (EDA), data preprocessing, hyperparameter tuning, and model deployment using a Flask API.

## Dataset Overview
- **Records:** Approximately 891 training samples (depending on the version)
- **Features:** 
  - **Key Features:** Passenger Class (Pclass), Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked
- **Target Variable:** `Survived` (0 = did not survive, 1 = survived)

## Key Analyses Performed

### Exploratory Data Analysis (EDA)
- **Univariate Analysis:** Examines distributions of Age, Fare, and other features.
  - Age distribution shows a mix of young and older passengers.
  - Fare distribution is skewed, with a few passengers paying very high fares.
- **Bivariate Analysis:** Explores relationships between features.
  - Strong relationship between Sex and survival.
  - Passenger class (Pclass) is also a significant predictor of survival.
- **Observations:**  
  - Missing values in Age and Cabin are handled during preprocessing.
  - Embarked and Fare also provide useful insights on survival trends.

### Data Preprocessing
- **Missing Value Imputation:**  
  - Fill missing values in Age using median imputation.
  - Handle missing Cabin values (e.g., via imputation or as a separate category).
- **Categorical Encoding:**  
  - Convert categorical features like Sex and Embarked using One-Hot or Label Encoding.
- **Feature Engineering:**  
  - Create new features (if applicable) from existing columns to boost predictive power.

### Predictive Modeling
- **Model Selection:**  
  - Common models include Logistic Regression, RandomForestClassifier, or XGBoost.
- **Hyperparameter Tuning:**  
  - Use `RandomizedSearchCV` or GridSearchCV to optimize model parameters.
- **Evaluation Metrics:**  
  - Accuracy, ROC-AUC, precision, recall, and confusion matrix.
- **Performance:**  
  - Initial experiments can be refined to boost the predictive performance.

### Model Deployment (Optional)
- **Flask API:**  
  - A lightweight API is built in `app.py` to serve real-time predictions.
  - The API accepts JSON input with passenger details and returns a survival prediction.



