# SYRIATEL-CUSTOMER-CHURN

![alt text](<images/churn Image.png>)

Author :**Nightingale Jeptoo**

A machine learning project that predicts customer churn for SyriaTel, a telecom company, using the CRISP-DM methodology. The aim is to identify customers likely to leave and help the company take proactive retention measures.

---

##  1. Business Understanding

- **Problem**: SyriaTel is facing significant customer churn, which directly impacts revenue and market share.
- **Objective**: Build a binary classification model to predict churn (`Yes` or `No`) and identify key drivers of customer departure.
- **Key Questions** I aim to address this:
What are the factors that are most strongly associated with churn.
Predict churn using early data
The services or customer segments that has the highest churn rates

- **Impact**: Insights can be used by the retention and marketing teams to reduce churn.

---

## 2. Data Understanding

- The dataset in use was obtained from **kaggle**. It contains SyriaTel telecom customers' information such as:

1. Account length.
2.  plan.
3. Voicemail plan.
4. Number of voicemail messages.
5. Total day, evening and night calls, charges and minutes.
6. Customer service calls.
7. Churn. Whether a customer left or not.

---

## 4. Exploratory Data Analysis (EDA)

- churn distribution by categorical features
![alt text](<images/churn distribution by categorical features.png>)
Interpreration

International Plan: Customers with an international plan have a relatively higher churn rate compared to those without one.

Voice Mail Plan: Customers with a voice mail plan have a lower churn rate compared to those without one.

- Count plots and group-wise churn rates for categorical features.
- Correlation heatmap.
- Key churn indicators discovered through visualizations.

---

##  5. Statistics

- **T-Tests**, **ANOVA**, and **Chi-Square** tests performed to evaluate significance of variables.
- Significant churn predictors validated statistically.

---

##  6. Machine Learning

### Models Used:
- Logistic Regression
- Random Forest
- XGBoost

### Evaluation Metrics:
- **Accuracy**, **ROC AUC**, **Precision**, **Recall**, **F1-Score**
- **Confusion Matrices**
- **ROC & PR Curves**
- **Feature Importance** visualizations



##  7. Findings & Recommendations

- **High churn likelihood** observed among:
  - Users with an **international plan**
  - Users making **frequent service calls**
  - Users with **higher day-time charges**
- Customers with a **voice mail plan** tend to churn less.
- **Recommendation**: Promote voicemail plan, reduce service issues, and target at-risk users for retention.

---

##  8. Conclusion

Machine learning models, especially **XGBoost**, were effective in predicting churn with high accuracy and AUC. The business can now leverage this model to implement a data-driven churn mitigation strategy.

---

##  Tools & Technologies

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Jupyter Notebook

---

 Contact
For questions or collaboration:

GitHub: Nightingale-Tech

Email: nigtingalemib@gmail.com

