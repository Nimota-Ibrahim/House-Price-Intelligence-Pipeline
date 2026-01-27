![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-black?style=for-the-badge&logo=xgboost&logoColor=white)

# House Price Intelligence Pipeline


## 1. Introduction
This project aims to predict residential property prices using a machine learning approach grounded in sound experimental practice. An **XGBoost-based pipeline** was developed, with all preprocessing steps fitted exclusively on the training data to prevent data leakage.

Beyond prediction, **the system integrates a decision-support layer** that automatically flags properties with significant pricing anomalies. This functionality reduces manual workload, allowing analysts to focus only on the listings requiring attention.

## 2. Performance Metrics
Model performance was evaluated primarily using **Mean Absolute Error (MAE)**. **k-fold cross-validation** was used to assess the stability of model performance across different data splits.

| Metric | Value (USD) | Interpretation |
| :--- | :--- | :--- |
| **Holdout MAE** | $15,445 | Performance on the specific validation split |
| **5-Fold CV Mean** | $15,613 | Expected performance across the whole dataset |
| **CV Std. Deviation** | $1,306 | Error variance (stability indicator) |

## 3. Key Methodology
* **Tree-Based Modeling:** Leveraged XGBoost, which handles non-linear relationships and feature distributions effectively without requiring manual scaling.
* **Leakage Prevention:** Ensured a strict separation between training and validation sets during the preprocessing phase.
* **Error Diagnosis:** Identified specific "Nightmare" outliers (indices 633, 1299, 689, 770) to understand where the model struggles and refine predictive reliability.

---
##### To view the full code and outlier analysis, open the [house_prediction_project.ipynb file](https://github.com/NimotaPro/House-Price-Prediction/blob/main/house_price_prediction_project.ipynb).
