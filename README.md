# 🩺 Diabetes Prediction using Machine Learning
This project applies multiple machine learning models to predict the likelihood of diabetes in patients based on health-related features. The goal was to compare different algorithms, tune hyperparameters, and evaluate performance using metrics such as **Accuracy, Precision, Recall, F1 Score, and ROC AUC**.

---

## 📊 Dataset
- Source: Pima Indians Diabetes Database (available on Kaggle / UCI ML Repo).
- Features include: glucose level, blood pressure, insulin, BMI, age, and more.
- Target variable: `Outcome` (0 = No Diabetes, 1 = Diabetes).

---

## ⚙️ Models Used
We trained and tuned the following models with **RandomizedSearchCV**:
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM

---

## 🔍 Workflow
1. **Data Preprocessing**
   - Handled missing/zero values
   - Standardized features for models sensitive to scaling (Logistic Regression, KNN)
   - Train-test split with stratification

2. **Model Training & Hyperparameter Tuning**
   - Used `RandomizedSearchCV` with 5-fold cross-validation
   - Optimized parameters like learning rate, max depth, n_estimators

3. **Evaluation**
   - Metrics: Accuracy, Precision, Recall, F1, ROC AUC
   - Plotted ROC Curves for comparison

---

## 📈 Results

| Model                 | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|------------------------|----------|-----------|--------|----------|---------|
| Logistic Regression    | 0.69     | 0.57      | 0.50   | 0.53     | 0.65    |
| KNN                    | 0.74     | 0.67      | 0.56   | 0.60     | 0.70    |
| Random Forest          | 0.75     | 0.71      | 0.55   | 0.62     | 0.71    |
| Gradient Boosting      | 0.75     | 0.67      | 0.58   | 0.62     | 0.71    |
| XGBoost                | 0.75     | 0.70      | 0.56   | 0.64     | 0.73    |
| **LightGBM (Best)**    | **0.77** | **0.70**  | **0.61** | **0.65** | **0.74** |

📌 **LightGBM achieved the best performance overall** with the highest ROC AUC of 0.74.

---

## 📉 ROC Curve

<img width="959" height="692" alt="Screenshot 2025-08-26 145909" src="https://github.com/user-attachments/assets/f45b5f03-e023-4dbd-84a7-c58f2a5321ae" />





