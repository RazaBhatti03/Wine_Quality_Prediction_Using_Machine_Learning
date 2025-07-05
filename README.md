#  Wine Quality Classification – Machine Learning Project

##  Problem Statement

To develop a machine learning model that accurately predicts the quality of wine based on its physicochemical properties such as acidity, sugar level, alcohol content, pH, sulphates, and other features provided in the WinequalityN dataset.

---

## **Business Goal**
The goal is to assist wine producers, quality control labs, and retailers in automating and improving the wine evaluation process. By predicting wine quality using data, businesses can:
- Save time and cost by reducing dependency on manual tasting panels.
- Improve quality control during production.
- Optimize production parameters to consistently produce high-quality wine.
- Gain competitive advantage by maintaining high standards and reducing human error.

---

##  Dataset

- **Source**: [Kaggle - UCI Wine Quality Dataset](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009)
- **Type**: Red and White wines
- **Records**: 6497
- **Target Feature**: `quality` (integer: 3 to 9, later binned into Low, Medium, High)
- **Features**: 11 physicochemical tests (e.g., acidity, alcohol, sulphates)

---

##  Technologies Used

| Category        | Tools/Packages                    |
|----------------|-----------------------------------|
| Language        | Python 3.x                        |
| Data Handling   | Pandas, NumPy                     |
| Visualization   | Matplotlib, Seaborn               |
| ML Algorithms   | Logistic Regression, Random Forest, Decision Tree |
| Evaluation      | Accuracy, F1-score, Classification Report |
| Feature Selection | RFE, L1 Regularization           |
| Imbalance Handling | SMOTE (imbalanced-learn)        |
| Deployment      | Streamlit / Flask (optional)      |

---

##  Exploratory Data Analysis (EDA)

- Checked correlations and distributions
- Detected & handled missing values, outliers, and label inconsistencies
- Outliers per feature were < 6%, hence retained

---

## 🧪 Feature Engineering

- **Binned `quality`** into:
  - `Low` (3–5), `Medium` (6–7), `High` (8–9)
- **Encoded** categorical features (`type`)
- **Balanced** the classes using **SMOTE**

---

##  Model Performance Summary

| Stage            | Model Used           | Accuracy (%) |
|------------------|----------------------|--------------|
|  Baseline Model | Logistic Regression  | **69.842**    |
|  Final Model    | Random Forest (Tuned + SMOTE) | **71.793**    |

- After applying feature selection, hyperparameter tuning, and class balancing (SMOTE), the final model showed an **improvement of ~2%** in accuracy compared to the baseline model. This reflects better generalization and more balanced classification across all wine quality classes.


---

##  Hyperparameter Tuning

- Used `GridSearchCV` (5-fold) to tune:
  - `max_depth`, `n_estimators`, `min_samples_leaf`, `max_features`, etc.
- Also tuned `penalty`, `C` in Logistic Regression

---

##  Handling Class Imbalance

| Class  | Before SMOTE | After SMOTE |
|--------|--------------|-------------|
| Low    | 1991         | 3184        |
| Medium | 3184         | 3184        |
| High   | 154          | 3184        |

 Improved **recall** and **F1-score** for minority class (`High`)

---

##  Deployment (Optional)

- Built a web app using **Streamlit**
- Accepts wine parameters from users
- Displays predicted wine quality category in real-time

---

##  Key Learnings

- Real-world data requires deep cleaning
- Accuracy is misleading on imbalanced data → use F1-score
- Feature selection boosts model simplicity and performance
- Deployment makes your ML project usable & impactful

---

## Insights

In the wine industry, **quality control** is a critical yet subjective and labor-intensive task. Wine quality is traditionally assessed by human tasters, which introduces **inconsistency**, **bias**, and **high operational costs**. For large-scale wine producers, this variability can affect customer satisfaction, brand reputation, and market value.

---

## How This Model Helps

By using **machine learning to classify wine quality**, wineries can:
- ✅ **Automate** the quality assessment process
- ✅ Ensure **consistent product standards**
- ✅ **Reduce costs** of hiring human experts for tasting
- ✅ Use data-driven insights to **optimize production & fermentation**
- ✅ Respond faster to quality issues in **real-time bottling lines**

The model predicts wine quality categories (Low, Medium, High) using chemical properties like acidity, alcohol, pH, etc., enabling **objective decision-making**.

---

## Conclusion & Business Impact

This project demonstrates how AI can replace traditional subjective methods in the wine industry. With an accuracy of **71.793%** after tuning, the model provides **reliable, scalable quality classification** that reduces human dependency and supports **data-driven quality control**.

✅ **Impact Summary**:
-  Saves time per batch
-  Reduces quality control costs
-  Improves product consistency & customer loyalty
-  Can be deployed in production lines for real-time decisions


---

## Connect with Me
Email: razabhatti03@gmail.com.com
LinkedIn: linkedin.com/in/yourname
Portfolio: yourportfolio.com

