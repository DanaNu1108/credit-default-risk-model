# 💳 Credit Card Default Prediction

This repository contains our implementation and analysis of machine learning models for predicting credit card default risk, based on the [UCI Default of Credit Card Clients dataset](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients).  
This work replicates and extends the findings from the research paper:  
**“The Comparisons of Data Mining Techniques for the Predictive Accuracy of Probability of Default of Credit Card Clients”** by I-Cheng Yeh and Che-hui Lien (2009).

---

## 📂 Project Structure
```
├── Default_Credit_Score.ipynb # Full notebook: EDA, modeling, evaluation
├── Final_Report.pdf # PDF report summarizing findings and methodology
└── README.md # Project documentation
```

---

## 🗃 Dataset

- Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)  
- Shape: (30,000 rows, 25 features)  
- Features: Demographics, credit limits, bill/payment history, and a binary target: `default.payment.next.month`

---

## 📒 Project Overview

We replicated models from the original research, including Logistic Regression, KNN, and Classification Trees. We also implemented and compared additional models such as SVM and XGBoost to evaluate potential improvements in predictive performance.

The analysis focuses on handling imbalanced data and evaluating models not just by accuracy but also by precision, recall, F1-score, and AUC.

---

## 📌 Key Insights

- `KNN` ranked best in training for identifying defaulters but lacked generalization.
- `ANNs` performed best in validation in the original paper. Our implementation with XGBoost achieved similar or better AUC and recall.
- `XGBoost` showed a strong balance between accuracy and minority class prediction.
- Pruned classification trees improved model interpretability and reduced overfitting.
- SMOTE was tested but resulted in overfitting; `scale_pos_weight` in XGBoost worked better.

---

## 🧠 Models Used

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Classification Trees
- Support Vector Machines (SVM)
- XGBoost

---

## 🧪 Notebook Summary

- Data cleaning (IQR filtering, outlier handling)
- Feature engineering and scaling
- Binary classification and evaluation
- Hyperparameter tuning (manual and grid search)
- Focused metrics: Accuracy, Precision, Recall, F1, AUC, Area Ratio

---

## 📑 View Final Report

📄 [Final_Report.pdf](./Final_Report.pdf)

---

## 🔗 References

- [UCI Dataset – Default of Credit Card Clients](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)
- [Research Paper on Semantics Scholar](https://www.semanticscholar.org/paper/The-comparisons-of-data-mining-techniques-for-the-Yeh-Lien/1cacac4f0ea9fdff3cd88c151c94115a9fddcf33)

---

## ✅ Final Notes

This project demonstrates practical application of research-backed models in financial risk analysis. XGBoost emerged as a strong performer for class imbalance, supported by precise model evaluation and calibration.
