# Heart Disease Prediction

## Overview
This project predicts the presence or absence of heart disease using the UCI Heart Disease dataset.

## Dataset
Source: UCI Machine Learning Repository

## Tools
- Python
- pandas
- matplotlib
- scikit-learn
- Jupyter Notebook

## Workflow
- data loading
- data cleaning
- binary target creation
- exploratory analysis
- categorical encoding
- train/test split
- model training
- evaluation and interpretation

## Models Used
- DummyClassifier
- Logistic Regression
- Decision Tree
- Random Forest

The logistic regression model classified 49 out of 60 test cases correctly, giving an accuracy of about 81.7%. It correctly identified 27 patients without disease and 22 patients with disease, but it also produced 5 false positives and 6 false negatives, so the main concern is that it still missed some real disease cases. In a health-related classification task, those false negatives matter because they are cases where the model predicted “no disease” even though disease was actually present.

## Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix

## Key Findings
- the baseline model performed worst, as expected
- the real models learned useful patterns from the features
- logistic regression provided a strong interpretable baseline
- random forest may provide stronger performance, depending on the split

## How to Run
1. Install requirements
2. Open the notebook
3. Run the cells in order
