# 🩺 Pima Indians Diabetes Prediction Model

A Machine Learning project using **Logistic Regression** to predict whether a patient has diabetes based on diagnostic medical measurements. 

This project covers data preprocessing (handling hidden zero-values), feature scaling, model training, evaluation, and model interpretation (feature importance). 

---

## 📌 Project Overview
The dataset originates from the **National Institute of Diabetes and Digestive and Kidney Diseases** (Pima Indians Diabetes Database). The goal is to diagnostically predict whether a patient has diabetes based on specific clinical features.

### Key Objectives:
- Identify and handle hidden missing values represented as zeros (`0`) in medical measurements.
- Preprocess and scale features using `StandardScaler` for distance-based optimization.
- Train a baseline **Logistic Regression** model for binary classification.
- Interpret feature coefficients to understand significant risk factors.

---

## 🛠️ Tech Stack & Libraries
- **Language:** Python
- **Data Manipulation:** `pandas`, `numpy`
- **Machine Learning:** `scikit-learn` (`LogisticRegression`, `StandardScaler`, `train_test_split`)
- **Model Evaluation:** `accuracy_score`, `classification_report`, `confusion_matrix`

---

## 🔄 Workflow & Pipeline

1. **Data Exploration & Cleaning:**
   - Identified hidden invalid zeroes in clinical features: `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI`.
   - Converted `0` values to `NaN` and imputed them using column **Medians** to preserve data integrity without dropping rows.

2. **Train-Test Split & Scaling:**
   - Split dataset into **80% Training** and **20% Testing** sets.
   - Scaled features using `StandardScaler` ($\mu=0, \sigma=1$) to optimize gradient descent performance.

3. **Model Training:**
   - Fitted a **Logistic Regression** classifier on the processed training set.

4. **Model Interpretation:**
   - Extracted model coefficients (`model.coef_`) to analyze feature importance.

---

## 📊 Key Results

- **Model Accuracy:** ~75.3%
- **Top Risk Factors (Coefficients):**
  1. **Glucose:** ~1.10 (Strongest positive predictor)
  2. **BMI:** ~0.68 (Second highest positive predictor)
  3. **Age:** ~0.39

---

