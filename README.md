# FIT-Competition-DataBASE

# 🌍 Sustainable Air Quality & Energy Analysis with Machine Learning

This project was developed for a data science competition focused on sustainability and climate change. Among **80 participating teams**, this project placed in the **🏆 Top 8 Finalists**, recognized for its innovative approach and strong analytical rigor.

---

## 🧠 Project Objective

To explore the relationship between global **air pollution** and **energy consumption** using open-source datasets and machine learning models. The goal was to generate actionable insights and predictive models to support **Sustainable Development Goals (SDGs)** and environmental policy-making.

---

## 📊 Datasets Used

- **Global Air Pollution Dataset**  
  Includes concentrations of major pollutants like **PM2.5**, **NO₂**, and **CO₂** across countries and years.

- **Sustainable Energy Dataset**  
  Contains data on **renewable and non-renewable energy** production, energy access, and electricity use by source.

---

## 🔍 Methodology Overview

### 1. **Data Cleaning**
- Standardized country names and formats  
- Removed null or irrelevant values  
- Harmonized temporal and spatial coverage

### 2. **Exploratory Data Analysis (EDA)**
- Identified patterns and correlations between energy types and air pollution  
- Visualized global trends and outliers

### 3. **Dataset Merging**
- Merged both datasets on `Country` and `Year` for integrated analysis

### 4. **Preprocessing & Feature Engineering**
- Scaled numerical features  
- Removed multicollinearity  
- Selected key predictors for modeling

### 5. **Machine Learning Models**
Used several regression models to predict pollutant levels:
- `Support Vector Regression (SVR)`
- `ElasticNet Regression`
- `Random Forest Regressor`
- `XGBoost Regressor`
- `Stacking Regressor` (ensemble of all models)

### 6. **Model Evaluation**
- Evaluated using **R²** and **RMSE**  
- Visualized **actual vs. predicted** pollution levels  
- Found **ensemble models** to be the most accurate and robust

---

## 🌱 Key Findings

- Countries with higher shares of **renewable energy** tend to have **lower emissions (PM2.5, CO₂)**  
- Ensemble models showed **strong predictive accuracy**, indicating complex relationships between variables  
- Energy access inequality is linked to higher pollution in some underdeveloped regions

---

## 🌍 Impact & Policy Implications

- Helps identify which energy policies are most effective for **emission reduction**  
- Supports progress tracking for **UN SDG 7 (Clean Energy)** and **SDG 13 (Climate Action)**  
- Provides data-driven insights for **governments and NGOs**

---

## 🛠 Tools & Technologies

- `Python`, `Pandas`, `NumPy`  
- `Scikit-learn`, `XGBoost`  
- `Matplotlib`, `Seaborn`  
- `Jupyter Notebook`

---

## 🏆 Competition Recognition

🎉 **Top 8 Finalist** out of 80 teams  
Recognized for exceptional integration of data, machine learning modeling, and sustainability relevance.
