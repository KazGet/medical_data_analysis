# Medical Risk Prediction with Logistic Regression

## 📌 Project overview
Binary classification task for predicting adverse cardiac outcomes
based on clinical, laboratory and echocardiographic features.

Dataset size: 210 patients  
Class imbalance: 159 negative / 51 positive

## 🎯 Objective
Build an interpretable baseline model with strong recall under class imbalance,
focusing on clinical applicability rather than complex ensembles.

## 🧠 Methodology
- Exploratory Data Analysis
- Missing values imputation (Iterative Imputer)
- Outlier analysis
- Correlation-based feature reduction
- Feature selection:
  - Mutual Information
  - RFECV (Logistic Regression, Random Forest, Gradient Boosting)
  - L1 / ElasticNet regularization
- Threshold optimization
- Cross-validation with F1-score

## 🏆 Final model
**ElasticNet Logistic Regression**

Selected features:
- ESC Pre-test Probability
- LVEDV rest
- Cholesterol
- LVESV  rest

Optimized decision threshold: **0.51**

### Performance (5-fold CV)
| Metric     | Value |
|-----------|-------|
| F1-score  | 0.541 |
| Precision | 0.465 |
| Recall    | 0.647 |
| Accuracy  | 0.733 |

## 📈 Key conclusions
- Logistic regression outperformed tree-based models on a small dataset
- Proper feature selection and threshold tuning significantly improved recall
- Model remains interpretable and clinically meaningful

## ⚠️ Limitations
- Small sample size
- No external validation
- Results should be interpreted as exploratory

## 🛠 Tech stack
Python, pandas, numpy, scikit-learn, catboost, matplotlib, seaborn
