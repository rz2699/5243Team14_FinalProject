# 5243Team14_FinalProject

# Laptop Price Prediction

This project aims to build supervised learning models to predict laptop prices based on technical specifications and brand-related features. We use data preprocessing, exploratory analysis, feature engineering, and multiple regression models to develop a final predictive model with strong performance.

---

## Dataset

- **Name:** Uncleaned Laptop Price Dataset  
- **Source:** [Kaggle – Laptop Prices](https://www.kaggle.com/datasets/ehtishamsadiq/uncleaned-laptop-price-dataset/data)  
- **Description:** Contains laptop features such as company, CPU/GPU brand, RAM, screen resolution, and operating system.

---

## Requirements

Make sure you have Python 3.8+ installed. Recommended environment: `conda` or `venv`

Install the required packages using pip:

`pip install pandas numpy matplotlib seaborn scikit-learn`

## How to Run the Project

You can run each notebook step-by-step in **Jupyter Notebook** or **VS Code with the Jupyter kernel**.

---

### 1. Data Cleaning

**Notebook:** `Data Cleaning.ipynb`

- Loads the raw Kaggle dataset
- Cleans missing values, standardizes formats, corrects types
- Saves output as:  
  ➤ `laptopData_CLEAN.csv`

---

### 2. Exploratory Data Analysis

**Notebook:** `EDA.ipynb`

- Performs exploratory data analysis on `laptopData_CLEAN.csv`
- Visualizes distributions and correlations
- Helps inform feature engineering decisions

---

### 3. Remove Outliers

**Notebook:** `Remove_Outliers.ipynb`

- Removes outliers from numerical columns using the IQR method
- Based on cleaned data from step 1
- Saves output as:  
  ➤ `laptopData_CLEAN_RemoveOutliers.csv`

---

### 4. Feature Engineering

**Notebook:** `Feature_Engineering.ipynb`

- Takes `laptopData_CLEAN_RemoveOutliers.csv` as input
- One-hot encodes categorical variables (brand, OS, etc.)
- Scales numerical features **(excluding `Price`)**
- Saves output as:  
  ➤ `laptopData_PROCESSED.csv`

---

### 4.5 Check Before Running Models or Analysis

Make sure the following files exist in your directory:

- `laptopData_CLEAN.csv`  
- `laptopData_CLEAN_RemoveOutliers.csv`  
- `laptopData_PROCESSED.csv`

---

### 5. Model Training

**Notebook:** `Models.ipynb`

- Loads `laptopData_PROCESSED.csv`
- Trains 3 models:
  - Linear Regression  
  - Random Forest Regressor (Tuned)  
  - Gradient Boosting Regressor (Tuned)
- Uses:
  - **80/20 Train-Test Split**
  - **5-Fold Cross Validation**
- Saves performance metrics and predictions

---

### 6. Model Analysis & Interpretation

**Notebook:** `Model Analysis.ipynb`

- Visualizes predicted vs. actual prices for all models
- Displays Random Forest feature importance plot
- Compares models using:
  - RMSE, MAE, R², and CV RMSE  
- Selects final model based on performance  
  ➤ **Gradient Boosting Regressor**
