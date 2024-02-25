

# Employee Attrition Prediction Project

## Overview
This project aims to predict employee attrition using machine learning techniques. Employee attrition, or turnover, is a critical challenge for organizations, as it impacts productivity, morale, and overall performance. By proactively identifying employees at risk of leaving, organizations can implement retention strategies to mitigate attrition and preserve valuable talent.

## Mechanism
The modeling process is divided into two phases:

### Phase 1: Imbalance Handling
Since the target variable (employee attrition) is imbalanced, this phase focuses on exploring different techniques to address class imbalance. Four different datasets are created:
1. **Imbalance Dataset**: The original dataset with imbalanced classes.
2. **Undersampling Dataset**: Random undersampling of the majority class to balance the classes.
3. **Oversampling (Random) Dataset**: Random oversampling of the minority class to balance the classes.
4. **Oversampling (SMOTE) Dataset**: Synthetic Minority Over-sampling Technique (SMOTE) to generate synthetic samples for the minority class.

The goal of this phase is to identify the best treatment for class imbalance based on model performance metrics.

### Phase 2: Model Improvement
In this phase, the focus shifts to improving the model's performance through feature engineering and feature selection techniques. Feature engineering involves creating new features or transforming existing ones to enhance predictive power. Feature selection aims to identify the most relevant features that contribute to predicting employee attrition.

## Model Selection
For this project, CatBoost, a gradient boosting algorithm, is chosen as the primary modeling technique. CatBoost is well-suited for handling categorical features and is robust to class imbalance.

## Usage
1. **Data Preparation**: Ensure the dataset containing relevant employee information and attrition labels is available.
2. **Phase 1 (Imbalance Handling)**:
   - Run the scripts to create four different datasets: imbalance, undersampling, oversampling random, and oversampling SMOTE.
   - Evaluate the performance of CatBoost models on each dataset using appropriate metrics (e.g., accuracy, precision, recall, F1-score).
3. **Phase 2 (Model Improvement)**:
   - Conduct feature engineering and feature selection techniques to enhance the model's predictive performance.
   - Retrain the CatBoost model on the improved dataset.
4. **Validation and Deployment**:
   - Validate the model's performance using cross-validation techniques.
   - Deploy the final model into production for making predictions on new employee data.

## Dependencies
- Python 3.x
- Libraries: pandas, scikit-learn, CatBoost, imbalanced-learn (for SMOTE)

