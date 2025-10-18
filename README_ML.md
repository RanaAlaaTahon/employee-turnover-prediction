# 🧩 Employee Attrition – Machine Learning Summary

## Overview

This project investigates the key factors influencing employee attrition using the IBM HR Analytics dataset.  
Machine learning models were developed to predict which employees are most at risk of leaving and to identify the strongest drivers of turnover.

## Machine Learning Process

1. **Data Preparation** – Cleaned and encoded categorical variables (e.g. `OverTime`, `Attrition`, `JobRole`),  
   treating ordinal and continuous features appropriately.
2. **Exploratory Analysis** – Examined attrition by satisfaction, tenure, overtime and income levels.
3. **Model Development** – Trained multiple tree-based models (**Decision Tree**, **Random Forest**, **Extra Trees**, **XGBoost**)  
   and optimised them using **GridSearchCV** with AUC, F1 and Recall scoring.
4. **Model Evaluation** – Compared performance using ROC-AUC, recall, F1 and balanced accuracy.  
   **Random Forest** and **XGBoost** emerged as the best-performing and most stable models.
5. **Interpretation** – Analysed feature importance and visualised results through precision–recall curves and confusion matrices.

## Key Findings vs Hypotheses

| Hypothesis | Outcome |
|-------------|----------|
| **1. Work–Life Balance** | Poor work–life balance is associated with higher attrition. |
| **2. Overtime** | Employees working overtime are significantly more likely to leave. |
| **3. Job Satisfaction** | Lower job satisfaction strongly correlates with higher attrition. |
| **4. Distance from Home** | Attrition increases with greater commuting distance. |
| **5. Career Growth** | Fewer promotions or shorter tenure with a manager increase attrition. |
| **6. Compensation** | Employees who left earned noticeably lower monthly income than those who stayed. |

## Conclusions

- **XGBoost** and **Random Forest** achieved the best balance between accuracy and recall.  
- **Recall-focused tuning** improved the ability to identify leavers without major loss of precision.  
- Findings support all six hypotheses, confirming that attrition is influenced by workload, satisfaction, tenure and pay equity.  
- Insights can guide HR teams to improve retention by promoting better work–life balance, fair compensation and career progression.

### Next Steps

- Train models with more extensive parameter grids.
- Optimise the training process by creating reuseable functions.
- Run models with Clustering & Regression algorithms.

---
