# Bank Account Fraud Detection

A machine learning project for detecting fraudulent bank account applications using supervised learning techniques.

## Project Overview

This project explores the use of machine learning to identify potentially fraudulent bank account applications.

The dataset contains approximately 1 million records with numerical and categorical features related to customer information, transaction/application behavior, and account details.

## Models Used

- Decision Tree Classifier
- Random Forest Classifier
- Linear Regression (baseline experiment)

## Data Preprocessing

The following preprocessing steps were performed:

- Exploratory Data Analysis (EDA)
- Missing-value analysis
- Handling missing values
- Analysis of numerical and categorical features
- Feature preprocessing using `ColumnTransformer`
- One-hot encoding of categorical variables
- Class imbalance analysis
- Train/validation/test split

## Model Experiments

### Decision Tree

Experiments were performed with:

- Maximum depth
- Gini vs Entropy
- Class balancing
- Probability threshold analysis

Final Decision Tree:

- Criterion: Gini
- Maximum depth: 5
- Class weight: Balanced

### Random Forest

Experiments were performed with:

- Maximum depth
- Minimum samples per leaf
- Class weighting
- Number of estimators

Final Random Forest:

- Number of estimators: 100
- Maximum depth: 25
- Minimum samples per leaf: 50
- Criterion: Gini
- Class weight: Balanced

## Final Test Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Decision Tree | 80.37% | 3.89% | 70.90% | 7.38% |
| Random Forest | **94.58%** | **10.55%** | 52.31% | **17.56%** |

## Conclusion

The Random Forest model performed better overall than the Decision Tree on the unseen test dataset.

Although the Decision Tree achieved higher fraud recall, it produced substantially more false positives. The Random Forest provided a better balance between precision and recall and achieved a higher F1 score.

Because the dataset is highly imbalanced, accuracy alone is not sufficient for evaluating fraud detection performance. Precision, recall, F1 score, and the confusion matrix are therefore given greater importance.

## Files

- `fraud_detection.ipynb` — Complete Jupyter/Google Colab notebook
- `.gitignore` — Prevents large datasets and unnecessary files from being uploaded

## Disclaimer

This project is intended for educational and experimentation purposes and should not be used as a production fraud detection system without further validation and testing.
