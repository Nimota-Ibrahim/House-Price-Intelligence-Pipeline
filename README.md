# Residential House Price Prediction

## 1. Introduction
This project aims to predict residential property prices using a machine learning approach grounded in sound experimental practice. An **XGBoost-based pipeline** was developed, with all preprocessing steps fitted exclusively on the training data to prevent data leakage.

Beyond predictive accuracy, the analysis emphasizes model robustness, interpretability, and transparent error diagnosis to reflect real-world valuation challenges.

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
##### To view the full code and outlier analysis, open the house_prediction_project.ipynb file.
