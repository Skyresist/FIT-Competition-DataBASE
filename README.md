# FIT-Competition-DataBASE

🌍 Sustainable Air Quality & Energy Analysis with Machine Learning
This project was developed for a data science competition focused on sustainability and climate change. Among 80 participating teams, this project placed in the Top 8 Finalists, recognized for its innovative approach and strong analytical rigor.

🧠 Project Objective
To explore the relationship between global air pollution and energy consumption using open-source datasets and machine learning models. The goal was to generate actionable insights and predictive models to support sustainable development goals and environmental policy-making.

📊 Datasets Used
Global Air Pollution Dataset
Includes concentrations of major pollutants like PM2.5, NO₂, CO₂ across countries and years.

Sustainable Energy Dataset
Contains data on renewable and non-renewable energy production, energy access, and electricity use by source.

🔍 Methodology Overview
1. Data Cleaning
Standardized country names and formats

Removed null or irrelevant values

Harmonized temporal and spatial coverage

2. Exploratory Data Analysis (EDA)
Uncovered patterns and correlations between energy types and air pollution

Identified outliers and global trends in emissions and energy practices

3. Dataset Merging
Merged both datasets on Country and Year to enable integrated analysis

4. Preprocessing & Feature Engineering
Scaled numerical features

Reduced dimensionality and handled multicollinearity

Selected most predictive features for modeling

5. Machine Learning Models
Built and evaluated several regression models to predict pollutant levels:

Support Vector Regression (SVR)

ElasticNet Regression

Random Forest Regressor

XGBoost Regressor

Stacking Regressor (ensemble approach combining all above models)

6. Model Evaluation
Assessed performance using R² and RMSE

Visualized actual vs. predicted pollutant values

Found ensemble models to perform most robustly across countries

🌱 Key Findings
Countries with higher shares of renewable energy tend to have lower PM2.5 and CO₂ emissions.

Ensemble models showed higher predictive accuracy, suggesting that pollutant levels are influenced by complex interactions between multiple energy indicators.

Energy access inequality was found to correlate with higher pollution in underdeveloped regions.

🌍 Impact & Policy Implications
Supports policymakers in identifying which energy reforms could have the greatest environmental benefit.

Helps organizations monitor progress toward UN SDG 7 (Affordable and Clean Energy) and SDG 13 (Climate Action).

🛠 Tools & Technologies
Python, Pandas, NumPy

Scikit-learn, XGBoost

Matplotlib, Seaborn

Jupyter Notebook

🏆 Competition Recognition
🎉 Top 8 Finalist out of 80 teams
This project stood out for its integration of real-world datasets, machine learning depth, and relevance to global sustainability challenges.
