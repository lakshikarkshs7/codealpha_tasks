# Credit Scoring Model

## Objective

The objective of this project is to predict an individual's creditworthiness using financial and credit-history-related information.

The model uses past financial and credit-related features to distinguish between lower-risk and higher-risk borrowers.

## Dataset

The dataset contains information related to borrowers, loans, income, employment, interest rates, and credit history.

Important features include:

- Person age
- Person income
- Employment length
- Loan amount
- Loan interest rate
- Loan intent
- Loan grade
- Home ownership
- Loan percentage of income
- Previous credit default history
- Credit history length

The target variable is `loan_status`, which represents the observed default outcome.

## Approach

The project follows these steps:

1. Data loading and exploration
2. Data cleaning
3. Duplicate removal
4. Missing-value handling
5. Exploratory Data Analysis (EDA)
6. Feature engineering
7. Categorical feature encoding
8. Numerical feature scaling
9. Train-test splitting
10. Model training
11. Model evaluation

### Feature Engineering

The following additional features were created:

- Income-to-loan ratio
- Estimated interest burden
- Credit history ratio
- Employment-age ratio

These features provide additional information about the borrower's financial capacity, loan burden, employment characteristics, and credit history.

## Machine Learning Models

Three classification algorithms were evaluated:

- Logistic Regression
- Decision Tree
- Random Forest

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

## Results

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 81.60% | 55.74% | 77.08% | 64.69% | 86.97% |
| Decision Tree | 91.81% | 88.94% | 71.44% | 79.23% | 90.22% |
| Random Forest | 93.03% | 92.07% | 74.54% | 82.39% | 93.16% |

## Key Findings

- Random Forest achieved the highest accuracy, F1-score, and ROC-AUC among the tested models.
- Logistic Regression achieved the highest recall for the higher-risk/default class.
- Financial capacity, loan burden, interest rate, employment characteristics, and credit-history-related features provided useful predictive information.
- Feature importance analysis showed that the income-to-loan ratio was one of the most influential features in the Random Forest model.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Files

- `credit_scoring_model.ipynb` — Jupyter Notebook containing data preprocessing, analysis, model training, evaluation, and visualizations.
- `credit_risk_dataset.csv` — Dataset used for the project.
- `README.md` — Project documentation.

## Conclusion

The credit scoring model demonstrates how machine learning classification algorithms can use financial and credit-history-related features to distinguish between lower-risk and higher-risk borrowers.

Among the tested models, Random Forest achieved 93.03% accuracy and a ROC-AUC of 93.16%, while Logistic Regression achieved the highest recall of 77.08% for the higher-risk/default class.
