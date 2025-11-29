# Home Credit Scorecard Model

This repository contains a complete credit risk modelling project using Logistic Regression and XGBoost to predict borrower default risk based on Home Credit’s historical loan data.

## Overview
The project applies exploratory data analysis, feature engineering, and predictive modelling to build a credit scorecard that helps improve lending decisions. Logistic Regression serves as the interpretable baseline model, while XGBoost is used as the champion model due to its ability to capture complex patterns.

## Data
Dataset is sourced from the Home Credit Default Risk competition and includes:
- application_train.csv: Main loan application data with target.
- bureau.csv: Customer credit bureau history.
- bureau_balance.csv: Monthly bureau balance records.
- HomeCredit_columns_description.csv: Column descriptions.

## Workflow
1. Load and inspect datasets.
2. Handle missing values and apply one-hot encoding.
3. Merge tables and engineer new features.
4. Split data using stratified sampling and scale features.
5. Train Logistic Regression and XGBoost models.
6. Evaluate models using ROC-AUC, accuracy, precision, recall, and F1-score.
7. Analyze feature importance.

## Results
| Model                | AUC   | Accuracy | Precision (1) | Recall (1) | F1-Score |
|---------------------|-------|----------|----------------|-------------|----------|
| Logistic Regression | 0.740 | 0.686    | 0.158          | 0.666       | 0.255    |
| XGBoost             | 0.761 | 0.707    | 0.169          | 0.671       | 0.270    |

### Key Insights
- EXT_SOURCE_1, EXT_SOURCE_2, and EXT_SOURCE_3 are the strongest predictors.
- Younger applicants tend to show a higher risk of default.
- Address and document inconsistencies significantly correlate with default risk.

## Installation
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn


## Usage
1. Clone the repository.
2. Open the notebook `Final_Task_Home_Credit_Scorecard_Model.ipynb`.
3. Ensure dataset files are available in the working directory.
4. Run all cells to reproduce the analysis and results.

## Project Structure
├── Final_Task_Home_Credit_Scorecard_Model.ipynb
└── README.md

