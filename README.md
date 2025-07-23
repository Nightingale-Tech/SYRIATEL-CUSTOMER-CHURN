# SYRIATEL-CUSTOMER-CHURN

![alt text](<images/churn Image.png>)

Author :**Nightingale Jeptoo**

A machine learning project that predicts customer churn for SyriaTel, a telecom company, using the CRISP-DM methodology. The aim is to identify customers likely to leave and help the company take proactive retention measures.

---

##  1. Business Understanding

- **Problem**: SyriaTel is facing significant customer churn, which directly impacts revenue and market share.
- **Objective**: Build a binary classification model to predict churn (`Yes` or `No`) and identify key drivers of customer departure.
- **Key Questions** I aim to address this:

1. What are the factors that are most strongly associated with churn.

2. Predict churn using early 

3. The services or customer segments that has the highest churn rates

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

###  churn distribution by categorical features

![alt text](<images/churn distribution by categorical features.png>)
Interpretation

International Plan: Customers with an international plan have a relatively higher churn rate compared to those without one.

Voice Mail Plan: Customers with a voice mail plan have a lower churn rate compared to those without one.

### Distribution of Numerical Features

![alt text](<images/distibution of Numerical Features.png>)
#### Intepretations

- **Normal Distributions**: Most usage-related features (minutes, calls, charges) are bell-shaped, indicating balanced behavior across the customer base.
- **Skewed Features**: `number vmail messages`, `total intl calls`, and `customer service calls` are highly skewed. These features may offer strong predictive power for churn.
- **Actionable Insight**: Features like high `customer service calls` are worth investigating in churn analysis as they may correlate with customer dissatisfaction.

#### Correlation Heatmap

![alt text](<images/correlation heat map.png>)
This correlation heatmap shows how strongly each variable relates to others.

*Churn*: Is positively correlated with international plan, total day charge, and customer service calls. It is negatively correlated with voice mail plan.

*Highly Correlated Pairs*: Strong positive correlations exist between total day minutes and total day **charge, total eve minutes and total eve charge, and total night minutes and total night charge. This is expected as charges are usually derived from minutes used.

*Low Correlations*: Most other variable pairs show very weak correlations (values close to 0.00).


##  5. Statistics

### 5.3 Hypothesis Testing

T-test – Difference in Means

Test if churned and non-churned customers differ significantly in features like total day minutes.

![alt text](<images/Total day images by churn.png>)

- t-statistic: -12.08  
- p-value: < 0.0001

There is a **statistically significant difference** in the average total day minutes between customers who churned and those who did not.  

The negative t-statistic suggests that churned customers tend to have higher daytime usage, which may indicate increased engagement before leaving, possibly due to unresolved service issues or dissatisfaction.


####  6. Machine Learning

### Models Used:
- Logistic Regression
- Random Forest
- XGBoost

### Evaluation Metrics:
- **Accuracy**, **ROC AUC**, **Precision**, **Recall**, **F1-Score**

#### Detailed Model Comparison

We compare the performance of the three classification models applied:

 #### Logistic Regression, Random Forest, and XGBoost.
---
### Performance Metrics

| **Metric**           | **Logistic Regression** | **Random Forest** | **XGBoost**       |
|----------------------|--------------------------|--------------------|--------------------|
| **Accuracy**         | 89.7%                    | 93.6%              | 94.1%              |
| **Precision**        | 72.2%                    | 83.3%              | 85.0%              |
| **Recall**           | 66.0%                    | 72.6%              | 78.2%              |
| **F1 Score**         | 69.0%                    | 77.6%              | 81.4%              |
| **AUC (ROC)**        | 0.81                     | 0.93               | 0.95               |


#### Summary

- **XGBoost** consistently outperforms the other models in all key metrics.
- It achieves the highest **accuracy**, correctly predicting 94.1% of churn outcomes.

- With a **precision of 85%**, it minimizes false positives, ensuring reliable churn alerts.

- It also has the highest **recall (78.2%)**, meaning it captures more actual churners than the others.

- The **F1 Score** of 81.4% reflects a strong balance between precision and recall.

- AUC (0.95) confirms that XGBoost is the most effective model at distinguishing between churners and non-churners.

Therefore, **XGBoost is the best-performing model** and recommended for deploment

- **Feature Importance** visualizations

![alt text](<images/Top 15 important Features.png>)

Summary Insight

International usage—measured by **call frequency**, **charges**, and **plan availability**—is the dominant churn signal. 

The **voice mail plan** acts as a proxy for service engagement, and **night call charges** add additional risk of churn.

##  7. Findings & Recommendations

 **High churn likelihood** observed among:
  - Users with an **international plan**

 **frequent service calls**
- Users with **higher day-time charges**
- Customers with a **voice mail plan** tend to churn less.

## Recommendation**:

**Target International Callers**  
   Identify users with high `total intl calls` or `intl charge` and proactively offer customized international plan

**Promote Voice Mail Plan Adoption**  
   Customers without a voice mail plan are at higher risk. Actions: Offer voice mail as part of bundled services

**Review Pricing for Key Periods**  
   Night and international usage costs strongly relate to churn.
   - Audit pricing policies

 **Monitor Usage Pattern Shifts**  
   Drops in call volume (across day, eve, night) can signal churn,set up alerts for rapid behavior changes  


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

Email: nightingalemib@gmail.com

