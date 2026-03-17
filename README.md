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
This project followed a complete binary classification workflow. The UCI Heart Disease dataset was loaded, inspected, and cleaned by handling missing values and converting columns to numeric format. The original target variable was transformed into a binary label representing absence or presence of heart disease.

Exploratory data analysis was performed to better understand the feature distributions and compare important variables across the two classes. Categorical variables were one-hot encoded, numeric features were scaled where needed, and the data was split into training and test sets.

A dummy baseline model was trained first, followed by logistic regression, decision tree, and random forest classifiers. The models were evaluated using accuracy, precision, recall, F1 score, ROC-AUC, and confusion matrices. Finally, model interpretation was performed using logistic regression coefficients and random forest feature importances.

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

## Findings

The logistic regression model performed reasonably well on the test set and provided a strong, interpretable baseline for the project.

### Main performance result
The model correctly classified **49 out of 60** test cases, giving an accuracy of about **81.7%**.

From the confusion matrix:
- **27** patients without heart disease were correctly classified as no disease
- **22** patients with heart disease were correctly classified as disease
- **5** patients without heart disease were incorrectly classified as disease
- **6** patients with heart disease were incorrectly classified as no disease

### Interpretation of the results
These results suggest that the model is able to detect useful patterns in the patient features and can separate the two classes reasonably well.

However, the most important limitation is the presence of **6 false negatives**. These are cases where the model predicted that the patient did not have heart disease even though the patient actually did. In a medical setting, false negatives are often more concerning than false positives because they represent missed positive cases.

### Precision and recall insight
The model achieved a good balance between precision and recall:
- Precision was about **81.5%**, meaning that when the model predicted heart disease, it was correct most of the time.
- Recall was about **78.6%**, meaning that it detected most, but not all, of the true disease cases.

This shows that the model is useful as a learning example, but still not strong enough to be treated as a reliable medical decision tool.

### Overall takeaway
This project demonstrated the full classification workflow on a real healthcare dataset:
- defining a binary prediction problem
- cleaning and preprocessing data
- training multiple models
- comparing performance using several evaluation metrics
- interpreting model errors through the confusion matrix

The project also showed why evaluation must go beyond accuracy. Even with a reasonably good overall score, the model can still make medically important mistakes.

## How to Run
1. Install requirements
2. Open the notebook
3. Run the cells in order
