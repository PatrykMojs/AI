# Time Series Trend and Categorical Feature Encoding Analysis

## 📌 Project Overview

This project presents a structured analytical workflow focused on:

- Linear trend modeling using multiple Python libraries
- Comparison of regression implementations
- Categorical feature encoding techniques
- Automated exploratory data analysis (EDA)
- Seasonality and trend decomposition using STL and MSTL

The objective is to demonstrate practical data preprocessing and modeling techniques commonly used in machine learning and time-series analysis.

---

## 📊 Dataset

The dataset contains retail transactional data including:

- Order date
- Store ID
- Staff ID
- Quantity
- List price
- Discount values

The dataset is aggregated and analyzed in both raw and time-series formats.

---

## 🛠 Technologies Used

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- scikit-learn
- statsmodels
- sweetviz

---

## 🔍 Project Structure

### 1️⃣ Data Preparation
- CSV loading
- Datetime conversion
- Data inspection

### 2️⃣ Linear Trend Modeling
Trendlines were estimated using:

- Plotly built-in trendline
- Statsmodels OLS regression
- Scikit-learn LinearRegression
- Seaborn regression plots

The results were compared to highlight differences in implementation and interpretation.

---

### 3️⃣ Categorical Feature Encoding

The following encoding methods were evaluated:

- `pd.get_dummies`
- `LabelEncoder`
- `OneHotEncoder`
- `LabelBinarizer`

Discussion includes:
- Risks of artificial ordinal relationships
- Dimensionality trade-offs
- Practical ML pipeline considerations

---

### 4️⃣ Automated EDA

Sweetviz was used to generate an automated exploratory report including:

- Distribution analysis
- Correlation detection
- Missing value insights

An interactive HTML report is included in the repository.

---

### 5️⃣ Seasonality and Trend Decomposition

Time-series decomposition was performed using:

- STL (Seasonal-Trend decomposition using Loess)
- MSTL (Multiple Seasonal-Trend decomposition)

This allows separation of:

- Trend component
- Seasonal component
- Residual component

The decomposition provides insight into structural behavior of the time series and prepares the dataset for forecasting.

---

## 📈 Key Insights

- Trend estimation varies depending on implementation.
- Proper date transformation is crucial in regression.
- One-hot encoding is preferred for nominal variables.
- Automated EDA tools significantly accelerate analysis.
- STL and MSTL enable effective decomposition of time-series data.

---