# Employee Performance and Retention Analysis

## Project Overview

This project aims to analyze the factors influencing employee performance and retention within a company. By leveraging machine learning models, we identify key drivers of attrition and build predictive models to help the organization proactively address potential retention issues and improve overall employee satisfaction and productivity.

## Dataset

The project utilizes the `Employee_Performance_Retention.csv` dataset. This dataset contains various attributes related to employees, including demographic information, work experience, performance ratings, job satisfaction levels, and ultimately, whether an employee has attrited.

## Methodology

The project follows a standard machine learning pipeline:

1.  **Data Loading and Exploration**: The dataset is loaded and initial explorations are performed to understand its structure and identify potential issues like missing values.
2.  **Preprocessing**:
    *   Categorical features are identified and handled using one-hot encoding.
    *   The data is split into features (X) and the target variable (y), which is employee attrition.
    *   The data is further split into training and testing sets for model development and evaluation.
    *   Numerical features are scaled using `StandardScaler` for models sensitive to feature scaling (like SVM).
3.  **Model Training and Evaluation**: Several machine learning models are trained and evaluated for their performance in predicting employee attrition:
    *   **Random Forest Classifier**: A tree-based ensemble model known for handling complex relationships and providing feature importance.
    *   **Support Vector Machine (SVM)**: Both Linear and Radial Basis Function (RBF) kernels are explored to capture different data patterns.
    *   **XGBoost Classifier**: A gradient boosting model often providing high accuracy.
4.  **Feature Importance Analysis**: For the Random Forest model, feature importance is analyzed to identify the most influential factors contributing to attrition.
5.  **Conclusion**: The performance of all trained models is compared based on accuracy to determine the best-performing model for this dataset.

## Results

The models were evaluated based on their accuracy on the test set.

| Model           | Accuracy |
| :-------------- | :------- |
| Random Forest   | 0.8033   |
| Linear SVM      | 0.8033   |
| RBF SVM         | 0.8033   |
| XGBoost         | 0.7817   |

Based on the accuracy scores, the Random Forest, Linear SVM, and RBF SVM models performed equally well and better than the XGBoost model in predicting employee attrition on this dataset. The feature importance analysis from the Random Forest model provides insights into the key factors driving attrition, which can be used by the organization for targeted interventions.

## Getting Started

To replicate this analysis, you will need a Python environment with the following libraries installed:

*   numpy
*   pandas
*   scikit-learn
*   xgboost

