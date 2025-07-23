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

## 3. Exploratory Data Analysis (EDA)

- churn distribution by categorical features
![alt text](<images/churn distribution by categorical features.png>)
Interpretation

International Plan: Customers with an international plan have a relatively higher churn rate compared to those without one.

Voice Mail Plan: Customers with a voice mail plan have a lower churn rate compared to those without one.

- Numerical Feature Distributions
![alt text](<images/distibution of Numerical Features.png>)
#### Intepretations

- **Normal Distributions**: Most usage-related features (minutes, calls, charges) are bell-shaped, indicating balanced behavior across the customer base.
- **Skewed Features**: `number vmail messages`, `total intl calls`, and `customer service calls` are highly skewed. These features may offer strong predictive power for churn.
- **Actionable Insight**: Features like high `customer service calls` are worth investigating in churn analysis as they may correlate with customer dissatisfaction.

- Correlation heatmap.
![alt text](<images/correlation heat map.png>)
This correlation heatmap shows how strongly each variable relates to others.

**Churn**: Is positively correlated with international plan, total day charge, and customer service calls. It is negatively correlated with voice mail plan.

**Highly Correlated Pairs**: Strong positive correlations exist between total day minutes and total day **charge, total eve minutes and total eve charge, and total night minutes and total night charge. This is expected as charges are usually derived from minutes used.

**Low Correlations**: Most other variable pairs show very weak correlations (values close to 0.00).
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

