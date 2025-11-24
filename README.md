Food Insecurity Prediction

Machine learning project using Python and XGBoost to model food insecurity across 3,000+ U.S. counties using USDA Food Environment Atlas data. Includes end-to-end workflow: preprocessing, exploratory analysis, model training, evaluation, and feature importance interpretation.

Project Overview

This project analyzes national food insecurity patterns and predicts county-level food insecurity rates for 2021–2023. Using socioeconomic and geographic variables from the USDA Food Environment Atlas, the project identifies the strongest drivers of food insecurity and evaluates the performance of an XGBoost regression model.

Dataset

Source: USDA Economic Research Service – Food Environment Atlas (2025 release)
Coverage: 3,000+ U.S. counties
Years: 2018–2020 and 2021–2023

# Key variables include:

Food Insecurity Rate

Very Low Food Security Rate

Change in Food Insecurity (2020–2023)

Poverty Rate

SNAP Participation

Median Income

Unemployment Rate

Dataset file: 2025-food-environment-atlas-data.xlsx

Data Processing and Analysis
Data Cleaning

Renamed columns for readability.

Removed sentinel values (-8888) and replaced with NaN.

Imputed missing values using medians.

Verified that all analysis variables were clean before modeling.

Exploratory Data Analysis

Examined distributions of food insecurity and very low food security.

Identified regional disparities, with southern states showing consistently higher food insecurity.

Performed correlation analysis to understand relationships between socioeconomic variables and food insecurity.

Observed temporal dependence: counties with high food insecurity in 2018–2020 tended to remain high in 2021–2023.

Key Insights

Food insecurity is not evenly distributed across the United States.

Poverty rate, unemployment, SNAP participation, and income showed the strongest relationships with food insecurity.

Southern states such as Arkansas, Mississippi, Louisiana, and Texas were consistently among the highest.

Machine Learning Model

Model Used: XGBoost Regressor
Target Variable: FoodInsecurityRate_2021_2023

Features

Historical food insecurity indicators

Changes in food insecurity

Very low food security rates

State-level dummy variables

Socioeconomic data such as poverty, unemployment, SNAP participation, and median income

Performance

R² score: approximately 0.98

Mean Absolute Error: roughly 1 percentage point

Predictions closely matched actual values, demonstrating high reliability.

Visualizations

The notebook includes:

Distribution plots for food insecurity indicators

State-level bar charts (Top 10 highest food insecurity rates)

Correlation heatmap

Actual vs. Predicted scatterplot

Residuals distribution

Feature importance bar chart

These visuals support the findings and provide interpretability for the model results.

Tools and Methods

Python

pandas, numpy

seaborn, matplotlib

scikit-learn

XGBoost

One-hot encoding

Regression modeling and evaluation metrics

Conclusion

This project demonstrates the use of machine learning to analyze county-level food insecurity and identify key socioeconomic drivers. The XGBoost model performed with high accuracy and highlights the importance of poverty, unemployment, SNAP participation, and income in predicting food insecurity. These insights can support data-driven decision-making aligned with Zero Hunger initiatives.
