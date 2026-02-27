# Exploratory Data Analysis – Retail Sales Dataset

## 📌 Project Overview

This project presents a comprehensive Exploratory Data Analysis (EDA) of a retail sales dataset.  

The goal of the analysis is to:

- Explore sales patterns over time
- Analyze distribution of prices and quantities
- Detect missing values
- Compare imputation strategies
- Identify potential outliers
- Prepare the dataset for machine learning modeling

This project demonstrates practical data preprocessing and visualization skills essential for machine learning workflows.

---

## 📊 Dataset Description

The dataset contains transactional retail sales data including:

- Order date
- Store information
- Staff information
- Product pricing
- Ordered quantity
- Discount values

The data was aggregated and analyzed across different time resolutions (daily and weekly).

---

## 🛠 Technologies & Libraries Used

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- missingno
- scikit-learn (SimpleImputer, KNNImputer)
- distfit

---

## 🔍 Key Analysis Steps

### 1️⃣ Data Loading & Preparation
- CSV import
- Date conversion
- Column cleaning
- Initial data inspection

### 2️⃣ Exploratory Visualizations
- Sales trends over time
- Orders by city and store
- Heatmaps (store vs month, weekday vs month)
- Interactive visualizations using Plotly

### 3️⃣ Distribution Analysis
- Histograms of prices and quantities
- Boxplots and violin plots
- Log transformation of skewed variables
- Statistical distribution fitting (distfit)

### 4️⃣ Missing Value Handling
- Numerical and percentage null analysis
- Missing data visualization (missingno)
- Comparison of:
  - Mean imputation
  - Median imputation
  - KNN imputation
  - Row removal (dropna)

### 5️⃣ Outlier Detection
- Histogram-based detection
- Scatterplot inspection
- Daily aggregation anomaly detection

### 6️⃣ Duplicate Detection
- Exact duplicate verification
- Aggregation-based duplicate checks

---

## 📈 Key Findings

- Sales show both weekly and seasonal patterns.
- Quantity distribution is right-skewed.
- Log transformation improves distribution symmetry.
- Missing data can be handled with different strategies depending on modeling goals.
- Outliers exist and should be treated carefully before applying ML algorithms.

---