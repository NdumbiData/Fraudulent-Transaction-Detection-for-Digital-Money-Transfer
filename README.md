---

# Fraudulent Transaction Detection for Digital Money Transfer

A machine learning project that detects fraudulent transactions in digital money transfer systems using advanced data analysis, classification models, and explainable AI techniques.

---

#  Overview

This project develops an end-to-end machine learning pipeline to classify transactions as **fraudulent or legitimate** within digital money transfer environments.

The solution follows a structured ML workflow:

* Data cleaning & preprocessing
* Exploratory Data Analysis (EDA)
* Feature engineering
* Model training & comparison
* Hyperparameter tuning
* Model evaluation
* SHAP explainability

### Strategic Focus

Due to the high financial risk associated with fraud in money markets, this project prioritizes **maximizing Recall** to minimize missed fraudulent transactions (false negatives).

In fraud-sensitive systems:

* A false positive can be reviewed.
* A false negative results in financial loss.

Therefore, the final model selection emphasizes **highest fraud recall performance**.

---

# 📊 Dataset Summary

The dataset consists of structured transaction records including:

### Transaction Features

* Transaction amount
* Transaction fee
* Timestamp
* Channel (mobile, web, ATM, etc.)
* Source and destination currency

### Customer Features

* KYC tier
* Account age
* Country information

### Risk & Behavioral Indicators

* Device risk score
* Velocity indicators
* Fraud-related flags
* Historical risk signals

Target Variable:

* `is_fraud`

  * 1 = Fraud
  * 0 = Legitimate

---

# Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* XGBoost
* LightGBM
* SHAP (Explainable AI)
* Jupyter Notebook

---

# Project Structure

```
Data_Sources_&_Initial_Assesment_.ipynb
│
├── Data loading & inspection
├── Initial structure review
└── Data quality assessment

Cleaning_notebook_(03_cleaning)_ipynb.ipynb
│
├── Data preprocessing
├── Handling missing values
├── Feature transformations
└── Chronological sorting (to prevent leakage)

EDA_&_Feature_Notebook_(04_features_eda_ipynb).ipynb
│
├── Exploratory Data Analysis
├── Risk pattern analysis
└── Feature engineering

Modelling , Tuning & SHAP.ipynb
│
├── Model training (Logistic Regression, Random Forest, XGBoost, LightGBM)
├── Class imbalance handling
├── Hyperparameter tuning
├── Cross-validation
└── SHAP explainability analysis
```

---

# Models Evaluated

The following classification models were trained and compared:

* Logistic Regression
* Random Forest
* XGBoost
* LightGBM

All models incorporated class balancing techniques.

---

# 📈 Model Performance

| Model               | Recall (Fraud) | ROC-AUC |
| ------------------- | -------------- | ------- |
| Logistic Regression | **0.94**       | 0.9816  |
| Random Forest       | 0.92           | 0.9738  |
| XGBoost             | 0.92           | 0.9642  |
| LightGBM            | 0.92           | 0.9648  |

### ✅ Selected Model: Logistic Regression

Logistic Regression achieved the **highest fraud recall (94%)**, making it the preferred model due to the project's strategic priority of minimizing undetected fraud.

---

# Evaluation Metrics

The following metrics were used:

* Precision
* Recall
* F1-Score
* ROC-AUC
* Accuracy

⚠️ Accuracy alone is not sufficient due to class imbalance.
The primary evaluation metric is **Recall for fraud class**.

---

# Explainability (SHAP)

SHAP was implemented to:

* Identify globally important fraud-driving features
* Explain individual transaction predictions
* Provide audit transparency
* Support regulatory compliance

This ensures the model is not a "black box" and can be trusted operationally.

---

# How to Run

```bash
git clone https://github.com/NdumbiData/Fraudulent-Transaction-Detection-for-Digital-Money-Transfer.git
cd Fraudulent-Transaction-Detection-for-Digital-Money-Transfer
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm shap jupyter
jupyter notebook
```

Open the notebooks sequentially to follow the project workflow.

---

#  Key Highlights

* End-to-end ML pipeline
* Chronological data split (real-world simulation)
* Hyperparameter optimization
* Cross-validation
* Recall-focused model selection
* Explainable AI integration (SHAP)
* Deployment-ready structure

---

# Author

**Ndumbi Kimani**
Data Scientist
GitHub: [https://github.com/NdumbiData](https://github.com/NdumbiData)

---
