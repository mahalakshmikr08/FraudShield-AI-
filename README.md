# 💳 FraudShield AI

## Intelligent Credit Card Fraud Detection & Risk Scoring System

FraudShield AI is a machine learning based credit card fraud detection system designed to identify potentially fraudulent transactions and assign a corresponding risk level.

The project focuses on handling the extreme class imbalance present in credit card fraud detection and evaluates machine learning models using precision, recall, F1-score and Precision-Recall AUC rather than relying only on accuracy.

---

## 🎯 Problem Statement

Credit card fraud is a major challenge because fraudulent transactions are extremely rare compared with legitimate transactions.

A conventional model can achieve very high accuracy by simply predicting most transactions as legitimate.

FraudShield AI addresses this problem using machine learning techniques designed for highly imbalanced classification.

The system:

- Detects potentially fraudulent transactions
- Handles severe class imbalance
- Compares multiple machine learning models
- Optimizes the classification threshold
- Produces a fraud probability
- Assigns a risk score
- Uses SHAP for model explainability
- Provides an actionable recommendation

---

## 🚀 Features

- Exploratory Data Analysis
- Fraud class imbalance analysis
- Feature preprocessing
- Logistic Regression
- Balanced Logistic Regression
- Random Forest
- XGBoost
- Precision-Recall analysis
- ROC analysis
- Threshold optimization
- Confusion matrix
- Feature importance
- SHAP Explainable AI
- Fraud probability
- Risk scoring
- Recommendation engine
- Interactive Gradio demo

---

## 📊 Dataset

The project uses the Credit Card Fraud Detection dataset from the Machine Learning Group of ULB.

Dataset source:

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Dataset characteristics:

- 284,807 transactions
- 492 fraudulent transactions
- 30 input features
- 1 target variable
- Extremely imbalanced fraud class

The dataset is not included in this repository because of its size.

---

## 🤖 Machine Learning Models

The following models were evaluated:

1. Logistic Regression
2. Balanced Logistic Regression
3. Random Forest
4. XGBoost

Models are compared using appropriate metrics for imbalanced classification.

---

## 📈 Evaluation Metrics

The project evaluates:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- PR-AUC
- Confusion Matrix

PR-AUC is given particular importance because fraud transactions represent only a very small percentage of the complete dataset.

---

## 🔍 Explainable AI

SHAP is used to identify the features that contribute to model predictions.

This allows the system to provide insight into why a transaction was classified as potentially fraudulent.

---

## 🚨 Risk Scoring

The predicted fraud probability is converted into a risk score from 0 to 100.

- 0–29: Low Risk
- 30–69: Medium Risk
- 70–100: High Risk

These thresholds are used as a decision-support policy for this academic prototype.

---

## 🛡️ Recommendation Engine

### Low Risk
Continue normal monitoring.

### Medium Risk
Consider additional verification.

### High Risk
Flag the transaction for manual review and additional customer verification.

---

## 🛠️ Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib
- Seaborn
- Gradio
- Imbalanced-learn
- Joblib

---

## 📁 Project Structure

```text
FraudShield-AI/
│
├── FraudShield_AI.ipynb
├── README.md
├── requirements.txt
│
├── FraudShield_models/
│   ├── fraud_model.pkl
│   ├── scaler.pkl
│   └── threshold.pkl
│
└── FraudShield_results/
    ├── model_comparison.csv
    └── threshold_analysis.csv

    ## 📊 Final Model Results

After evaluating multiple machine learning models, XGBoost was selected based on the experimental results.

| Metric | Result |
|---|---:|
| Best Model | XGBoost |
| Decision Threshold | 0.60 |
| Precision | 88.17% |
| Recall | 83.67% |
| F1 Score | 85.86% |
| PR-AUC | 87.89% |

The optimized decision threshold of 0.60 was selected based on the precision-recall trade-off and F1 score.

Because credit card fraud is a highly imbalanced classification problem, PR-AUC, precision, recall and F1 score are emphasized instead of relying only on accuracy.
