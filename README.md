# Employee Burnout Analysis and Prediction

## Project Overview

This project focuses on analyzing employee-related factors and building a machine learning model to predict employee Burn Rate.

The project includes data cleaning, exploratory data analysis (EDA), data preprocessing, machine learning model comparison, cross-validation, and hyperparameter tuning.

## Dataset Features

The dataset contains information such as:

- Gender
- Company Type
- WFH Setup Available
- Designation
- Resource Allocation
- Mental Fatigue Score
- Burn Rate

The target variable for prediction is **Burn Rate**.

## Data Preprocessing

The following preprocessing steps were performed:

- Removed rows with missing target values (Burn Rate)
- Filled missing Resource Allocation and Mental Fatigue Score values using median imputation
- Removed Employee ID
- Analyzed and removed Date of Joining
- Converted categorical variables into numerical features using one-hot encoding
- Split the dataset into 80% training data and 20% testing data

## Machine Learning Models

The following regression models were evaluated:

1. Linear Regression
2. Random Forest Regressor
3. Gradient Boosting Regressor
4. Extra Trees Regressor

## Model Performance

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 0.05346 | 0.07093 | 0.86792 |
| Random Forest | 0.04960 | 0.06424 | 0.89165 |
| Gradient Boosting | 0.04832 | 0.06175 | 0.89988 |
| Extra Trees | 0.05098 | 0.06619 | 0.88499 |

Gradient Boosting achieved the best performance among the initially evaluated models.

## Cross-Validation

5-fold cross-validation was performed on the Gradient Boosting model.

- Average Cross-Validation R²: **0.90265**
- Standard Deviation: **0.00418**

## Hyperparameter Tuning

GridSearchCV was used to tune the Gradient Boosting model.

Best parameters:

- Learning Rate: 0.1
- Max Depth: 4
- Number of Estimators: 200

## Final Model Performance

The tuned Gradient Boosting Regressor achieved:

- MAE: **0.04697**
- RMSE: **0.05985**
- R² Score: **0.90594**

The tuned Gradient Boosting Regressor was selected as the final model.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- Joblib

## Model File

The trained model is saved as:

`employee_burnout_model.pkl`

## Dataset Attribution

The dataset used in this project was obtained from an external source and is not claimed as original work. Dataset source and licensing information should be reviewed before redistribution.

## Disclaimer

This project is intended for educational and machine learning demonstration purposes. The predicted Burn Rate should not be interpreted as a medical or clinical assessment.
