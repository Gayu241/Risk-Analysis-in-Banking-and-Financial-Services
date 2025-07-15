# 📊 Loan Default Risk Analysis – Exploratory Data Analysis (EDA)

## 📝 Problem Statement
This project focuses on understanding risk analytics in the banking and financial services domain using exploratory data analysis. The goal is to identify patterns that indicate whether a client is likely to face payment difficulties when granted a loan. This analysis helps financial institutions make informed decisions on loan approval, amount, or interest rate to minimize financial losses.

## 📁 Dataset Overview
The analysis is based on three datasets:

1. **application_data.csv** – Contains information about clients at the time of application.
2. **previous_application.csv** – Includes data on the clients' previous loan applications.
3. **columns_description.csv** – A data dictionary explaining all features.

## 🎯 Business Objective
- Identify key variables influencing loan default.
- Use EDA to differentiate between clients likely to repay vs. those likely to default.
- Help financial institutions reduce credit risk and avoid rejecting creditworthy applicants.

## 🔍 Analysis Workflow

### 1. **Data Cleaning & Preprocessing**
- Loaded and explored both application and previous loan datasets.
- Merged where necessary to bring more context into the application data.
- Identified and handled missing values using logical imputation strategies (mean/median/mode) or column elimination for high-missing-value features.
- Converted data types and handled inconsistent values.

### 2. **Outlier Detection**
- Detected outliers using boxplots and statistical thresholds (IQR, Z-score).
- Highlighted rather than removed outliers as part of insight generation.

### 3. **Data Imbalance Check**
- Checked distribution of the target variable (`TARGET`):
  - `0` – Client did not face payment difficulties.
  - `1` – Client had payment difficulties.
- Found class imbalance (minority class ≈ 8% of data).
- Visualized imbalance using count plots and pie charts.

### 4. **Univariate Analysis**
- Examined individual variables like income, credit amount, loan duration, etc.
- Identified suspicious or meaningful distributions in target segments.

### 5. **Bivariate/Segmented Analysis**
- Segmented numerical and categorical variables by `TARGET`.
- Used bar plots, KDE plots, and boxplots to understand relationships and distributions.
- Identified variables like `EXT_SOURCE_3`, `AMT_INCOME_TOTAL`, `DAYS_EMPLOYED`, etc. as strong differentiators.

### 6. **Correlation Analysis**
- Created separate correlation matrices for clients with (`TARGET = 1`) and without (`TARGET = 0`) payment difficulties.
- Identified top 10 variable pairs (excluding `TARGET`) in both groups to find differences in relationships between variables across segments.

### 7. **Visualisations**
- All visualizations were created using Python (Seaborn, Matplotlib, Plotly).
- Optional enhancement done using Tableau for presentation aesthetics.


## 🧠 Tools & Libraries Used
- Python (Pandas, NumPy, Seaborn, Matplotlib, Plotly)
- Jupyter Notebook
- Tableau (for optional enhanced visuals)
- sklearn (for data preprocessing support)
