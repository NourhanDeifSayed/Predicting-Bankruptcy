
## 📌 Project Overview

Bankruptcy prediction is a critical task for investors, banks, and stakeholders. Using financial data from 6,819 Taiwanese companies (1999–2009), we trained and evaluated a range of machine learning models to predict whether a company is at risk of bankruptcy.

We incorporated **XAI techniques** (SHAP, LIME, PDP, ICE, and surrogate models) to make these "black-box" models interpretable and trustworthy.

---

## 🎯 Objectives

- 📊 Analyze 96 financial features including profitability, liquidity, and leverage ratios.
- 🤖 Train and compare ML models: Logistic Regression, SVM, Random Forest, XGBoost, AdaBoost, LightGBM, Neural Networks.
- 📈 Evaluate model performance using accuracy, precision, recall, F1-score, AUC.
- 🧩 Apply XAI tools to explain feature influence on predictions.

---

## 🧠 Machine Learning Models Used

| Model                  | Accuracy | Notes                                             |
|------------------------|----------|---------------------------------------------------|
| Random Forest          | 98.5%    | Top performer with high generalization            |
| XGBoost                | 96.2%    | Balanced performance & scalable                   |
| SVM (RBF Kernel)       | 97%      | Effective but lower recall on minority class      |
| Logistic Regression    | 96.7%    | Strong baseline with great interpretability       |
| AdaBoost               | 96%      | High accuracy but poor recall (overfit risk)      |
| Neural Network         | 85%      | Best for recall but weaker on precision           |

---

## 🧪 Data & Preprocessing

- **Source:** [Taiwan Economic Journal via Kaggle](https://www.kaggle.com/datasets/fedesoriano/company-bankruptcy-prediction)
- **Features:** 96 financial ratios per company
- **Target:** `Bankrupt?` (1 = bankrupt, 0 = non-bankrupt)
- **Preprocessing:** 
  - No missing values
  - Standardized with `StandardScaler`
  - Train/test split: 80% / 20%
  - Handled class imbalance using `SMOTE`

---

## 🧠 Feature Selection

Used **Recursive Feature Elimination (RFE)** to select the top 10–30 most relevant features for each model. This improved both model interpretability and generalization.

---

## 🕵️‍♀️ XAI Techniques Applied

| Technique       | Purpose |
|----------------|---------|
| **SHAP**       | Global & local feature contributions |
| **LIME**       | Local interpretable model approximation |
| **PDP / ICE**  | Visualize marginal/individual feature effects |
| **Surrogate Trees** | Translate complex model into interpretable decisions |
| **Permutation Importance** | Feature impact ranking |

---

## 📈 Key Insights

- **Net Income to Total Assets**, **Persistent EPS**, and **Operating Profit Rate** were the most influential features.
- SMOTE significantly improved recall on bankrupt cases.
- XAI methods provided actionable insights for understanding model decisions.
- The Random Forest model provided the best balance of performance and explainability.

---

## 🏁 Conclusion

This project showcases how machine learning, when combined with explainable AI, can offer powerful and transparent solutions to financial risk prediction. Our work contributes not only accurate models but also interpretable explanations that support trustworthy decision-making.

---

