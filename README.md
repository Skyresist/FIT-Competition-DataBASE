# Air Quality Prediction & Energy Recommender — FIT Competition 2025

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Skyresist/FIT-Competition-DataBASE/blob/main/dataBASE.ipynb)
![Result](https://img.shields.io/badge/Result-Top%208%20of%2080%20teams-6f42c1)

Team **DataBASE**'s entry for the **FIT Competition 2025** (sustainability & climate theme), which reached the **Top 8 finalists out of 80 teams**.

The project links a country's **air quality** to how it **produces and consumes energy**, then turns that into a tool: enter a country (or a new set of pollution and energy figures) and get a predicted Air Quality Index plus rule-based energy-policy recommendations.

## Pipeline

1. **Clean** — 23,463 city-level air-pollution records (CO, O₃, NO₂, PM2.5 and overall AQI); 23,035 remain after removing missing and invalid rows.
2. **Aggregate** — average AQI values per country.
3. **Merge** — join with the Global Sustainable Energy dataset (2020: electricity from fossil, nuclear and renewable sources; energy use per capita) to build one modelling table covering 154 countries.
4. **Explore** — pollutant distributions, top fossil-fuel producers, energy mix vs. air quality.
5. **Model** — tune each model with 5-fold `GridSearchCV` on an 80/20 train–test split, and record training time and peak memory for each.
6. **Recommend** — rule-based recommendations driven by a country's AQI level, energy mix and consumption.
7. **Prototype** — interactive notebook cells for looking up a country or entering new values.

## Models compared

| Model | Test RMSE | Test R² |
|---|---:|---:|
| Support Vector Regression | 4.42 | 0.979 |
| ElasticNet | 3.94 | 0.983 |
| Random Forest | 3.85 | 0.984 |
| XGBoost | 3.21 | 0.989 |
| **Stacking ensemble** | **3.20** | **0.989** |

Blending and voting ensembles were also tested.

## Limitations — what I'd do differently

The overall AQI is defined from the individual pollutant sub-indices, and those sub-indices were model inputs. That makes the target largely recoverable from the features, which explains the near-perfect R² across every model; these scores overstate real predictive power.

A revised version would:
- **drop the pollutant sub-indices** and predict AQI from energy and socio-economic variables only. This is the question the project actually cares about: how much does a country's energy mix explain its air quality?
- use **group-aware cross-validation** by country, so the same country never appears in both train and test.

## Tools

Python · pandas · NumPy · scikit-learn · XGBoost · Matplotlib · Seaborn · Jupyter / Colab

## Files

| File | Contents |
|---|---|
| `dataBASE.ipynb` | Full workflow: cleaning, EDA, merging, modelling, recommender, prototype |
| `global air pollution dataset.csv` | City-level AQI data |
| `global-data-on-sustainable-energy (1).csv` | Country-level energy data |
