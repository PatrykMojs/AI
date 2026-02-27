# Model Selection, Evaluation Metrics and Experiment Tracking with MLflow

## 📌 Project Overview

This project presents a complete machine learning workflow for classification problems, including:

- Evaluation under class imbalance
- Comparison of multiple ML models
- Hyperparameter tuning using cross-validation
- Experiment tracking with MLflow
- Visualization of underfitting vs overfitting

The objective is to demonstrate a production-oriented ML experimentation pipeline rather than a simple lab exercise.

---

## 📊 Dataset

The dataset contains physiological and motion-related sensor measurements with a target classification label.

> ⚠ Dataset files are not included in this repository due to size limitations.
>
> To run this notebook locally, provide:
> - `nurse_data_train.csv`
> - `nurse_data_test.csv`

---

## 🔍 Project Workflow

### 1️⃣ Evaluation Metrics and Class Imbalance

The project demonstrates why accuracy alone can be misleading in imbalanced classification tasks.

Metrics used:
- Accuracy
- Precision (macro)
- Recall (macro)
- F1-score (macro)
- Balanced Accuracy
- Cohen’s Kappa
- ROC-AUC (OvR)
- Confusion Matrix

This ensures realistic model evaluation.

---

### 2️⃣ Handling Imbalance (SMOTE)

SMOTE (Synthetic Minority Oversampling Technique) is applied as an optional experiment to improve minority class representation.

Its impact is evaluated using the same metric set and confusion matrix analysis.

---

### 3️⃣ Hyperparameter Tuning with Cross-Validation

Models tuned using GridSearchCV:

- DecisionTreeClassifier
- RandomForestClassifier
- MLPClassifier
- LogisticRegression
- SVC
- KNeighborsClassifier

Cross-validation is used to:
- Reduce variance in model evaluation
- Prevent overfitting to a single train/test split
- Select robust hyperparameters

Scoring metric: **F1-macro**

---

### 4️⃣ Feature Importance and Interpretability

For selected models:

- Decision Tree
- Random Forest
- Logistic Regression

Feature importance or coefficient magnitudes are analyzed to improve interpretability.

---

### 5️⃣ Experiment Tracking with MLflow

MLflow is used to:

- Log model parameters
- Track evaluation metrics
- Store trained models
- Compare multiple runs

Sklearn autologging is enabled to simplify experiment tracking.

To run MLflow locally:

```bash
pip install mlflow
mlflow ui --host 127.0.0.1 --port 5000