# BankDatasetModelComparison
# Classification Model Comparison and Tuning

Hello everyone, my name is **Akash Rane**, and this is  Classification Modeling**.

---

## 📌 Objective

The goal of this notebook was to analyze a dataset and build classification models to predict whether a customer would subscribe to a term deposit. I evaluated multiple machine learning algorithms **before and after hyperparameter tuning** to compare their performance.

---

##  Models Used

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Decision Tree
4. Random Forest
5. Naive Bayes
6. XGBoost

Each model was evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score
- ROC Curve and AUC

---

## Hyperparameter Tuning

For each model, I used **GridSearchCV** to tune important parameters like:
- `C`, `solver` for Logistic Regression
- `n_neighbors` for KNN
- `max_depth`, `min_samples_split` for Decision Tree and Random Forest
- `learning_rate`, `n_estimators` for XGBoost
- `var_smoothing` for Naive Bayes

Tuning was performed using **F1 Score** as the scoring metric with **3-fold cross-validation**.

---

##  Results Summary

After tuning, we observed improvements in multiple models. Key highlights:

- **XGBoost** gave the best overall performance with an F1 Score of **0.59**, Accuracy of **0.92**, and balanced Precision and Recall.
- **Random Forest** and **Decision Tree** also showed strong improvements.
- **Naive Bayes** had the highest **Recall (0.62)** but low Precision, useful if false negatives are critical.
- **Logistic Regression** had strong Precision but suffered in Recall after tuning.

---

## Metric Focus

Depending on the business goal:

- If we want to **avoid false positives**, we focus on **Precision**.
- If we want to **capture all positives**, we focus on **Recall**.
- In this project, since both matter, we used **F1 Score** as our key comparison metric.

---

##  Final Model Recommendation

I recommend using **XGBoost** as it consistently performed the best across all evaluation metrics after tuning. It strikes a great balance and is ideal.

---

# Thank you!

