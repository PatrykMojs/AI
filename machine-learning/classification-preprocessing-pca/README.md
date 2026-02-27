# Classification Preprocessing and Dimensionality Reduction (PCA)

## 📌 Project Overview

This project presents a complete machine learning preprocessing workflow for a classification task.

The analysis includes:

- Data exploration
- Feature engineering
- Correlation analysis
- Dimensionality reduction using PCA
- Feature scaling
- Train / validation / test split strategies

The objective is to demonstrate practical ML data preparation techniques used before training classification models.

---

## 📊 Dataset

The dataset contains physiological and motion-related sensor measurements collected over time, including:

- X, Y, Z motion signals
- EDA (electrodermal activity)
- HR (heart rate)
- TEMP (temperature)
- Timestamp
- Subject ID
- Target label (classification)

> ⚠ The dataset file (`nurse_data.csv`) is not included in this repository due to size limitations.

To run this notebook locally, place the dataset file in the same directory as the notebook.

---

## 🔍 Project Workflow

### 1️⃣ Data Loading and Cleaning
- Datetime parsing
- Aggregation by subject and time
- Numeric transformation of time-of-day
- Basic data quality checks

---

### 2️⃣ Exploratory Analysis
- Feature distributions
- Target label distribution
- Correlation heatmap
- Time-series visualization for individual subjects

---

### 3️⃣ Feature Engineering

Custom features were created to enrich the dataset:

- `EDA_TEMP_diff` – difference between electrodermal activity and temperature
- `hand_distance` – motion magnitude from X/Y/Z signals
- `EDA_change_rate` – rate of change in EDA
- `activity_percentage` – estimated daily activity ratio
- Time-based features (weekday, time of day)

Categorical features were encoded using one-hot encoding.

---

### 4️⃣ Dimensionality Reduction (PCA)

Principal Component Analysis was applied to:

- Reduce feature space dimensionality
- Address multicollinearity
- Preserve maximum variance

Explained variance ratios were analyzed to determine information retention.

---

### 5️⃣ Scaling and PCA Comparison

MinMaxScaler was applied to normalize features before PCA.

Key observation:
- PCA results significantly depend on feature scale.
- Scaling ensures balanced contribution of all variables.

---

### 6️⃣ Train / Validation / Test Split

The dataset was divided into:

- Training set
- Validation set
- Test set

Both random and stratified splitting strategies were analyzed.

Stratified splitting is recommended for classification tasks to preserve class proportions.

---

## 📈 Key Insights

- Feature scaling strongly impacts PCA behavior.
- Engineered features improve representation of physiological signals.
- Stratified splitting is essential when class imbalance exists.
- Proper preprocessing is critical before model training.

---