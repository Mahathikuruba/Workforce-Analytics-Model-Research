# 1. Machine Learning Model Research

## Problem definition

Employee attrition prediction is a **binary classification** problem:

- `Yes` = employee left the organization
- `No` = employee stayed

The model uses workforce attributes such as age, department, job role, monthly income, overtime, job satisfaction, years at company and other available employee features.

The objective is to estimate the likelihood of employee attrition and support proactive retention planning.

## Candidate models

### Logistic Regression

A supervised classification algorithm used as a baseline.

**Advantages:** simple, fast and relatively interpretable.

**Limitation:** the basic model mainly captures linear relationships.

### Decision Tree

A tree-based classifier that makes predictions through feature-based decisions.

**Advantages:** easy to visualize and explain; captures nonlinear relationships.

**Limitation:** a single tree can overfit the training data.

### Random Forest

An ensemble of many decision trees.

**Advantages:** suitable for tabular data, captures nonlinear relationships, robust compared with a single tree, and provides feature-importance information.

**Limitation:** less directly interpretable than one small decision tree.

### Gradient Boosting

Builds trees sequentially so that later trees improve errors made by earlier trees.

**Advantages:** often performs strongly on structured/tabular datasets.

**Limitation:** requires more tuning and can overfit if not controlled.

## Model evaluation

The project can compare models using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrix

For an attrition early-warning system, recall is important because a false negative means a potentially departing employee was not flagged. Precision is also important because too many false alerts can waste HR resources.

Therefore, the final model should be selected using a balance of predictive performance, interpretability and business usefulness rather than accuracy alone.

## Proposed model selection

Random Forest is a strong candidate for structured workforce data because HR datasets contain nonlinear relationships between employee attributes. However, the final model should be selected from the actual experimental results in the Python task rather than claiming a model is best without testing.

## Explainable AI

HR users need to understand why a model produced a high-risk prediction.

For example:

> Attrition risk: High

Possible contributing factors could include overtime, low job satisfaction, short tenure or other features identified by the model.

**SHAP (SHapley Additive exPlanations)** can be used to explain how features contribute to individual predictions and overall model behavior.

### Reference

Lundberg, S. M. and Lee, S.-I. (2017), *A Unified Approach to Interpreting Model Predictions*.
