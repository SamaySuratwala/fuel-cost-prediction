# Predicting Annual Fuel Costs — STOR 320.002 Group 16

**Course:** STOR 320: Introduction to Data Models and Inference  
**Date:** Spring 2026 | University of North Carolina at Chapel Hill  
**Team:** Alexa Kislowski, Cooper Lair, Annabelle Lawson, Akshita Padala, Samay Suratwala

---

## Overview

This project analyzes the **2025 EPA Fuel Economy Dataset** to identify vehicle characteristics that predict annual fuel cost and to examine the relationship between transmission type and combined fuel efficiency. The dataset covers 868 vehicle configurations across 23 manufacturers and 20 vehicle classes.

**Research Questions:**
1. Are there vehicle characteristics that can predict the average annual cost of fuel?
2. Is there an association between transmission type and combined fuel efficiency?

---

## Repository Contents

| File | Description |
|------|-------------|
| `Group_16_2025_Fuel_Economy_Dataset.csv` | Cleaned 2025 EPA Fuel Economy dataset (868 observations) |
| `Group_16_EDA_Fuel_Efficiency.pdf` | Exploratory Data Analysis — initial questions, visualizations, and follow-up investigation |
| `Fuel_Cost_Prediction_Presentation_Group_16.pdf` | Final presentation slides (April 29, 2026) |
| `STOR_320_Final_Paper.pdf` | Final written report with full methodology, results, and conclusions |

---

## Key Findings

- **Combined fuel efficiency** is the strongest predictor of annual fuel cost (β = −73.13 per MPG, p < 0.0001)
- **Cylinder count** adds approximately $160 per additional cylinder (p < 0.0001)
- **AWD and 4WD** drivetrains carry a statistically significant annual cost premium (~$125–$149) relative to front-wheel drive
- **Transmission type** is significantly associated with combined fuel efficiency (one-way ANOVA, F = 111.48, p < 0.0001)
- The multiple linear regression model explains **87.7% of variance** in annual fuel cost (Adjusted R²)
- **XGBoost** outperformed all other models (RMSE = 183.48, R² = 0.9425), confirming nonlinear structure in the data

---

## Methods

- Correlation matrix analysis
- Simple and multiple linear regression
- One-way ANOVA
- Random Forest (variable importance)
- 5-fold cross-validated model benchmarking: OLS, Elastic Net, Quantile Regression, Bayesian Regression, Decision Tree, Random Forest, XGBoost

---

## Data Source

U.S. Environmental Protection Agency. (2025). *2025 Fuel Economy Guide*. [fueleconomy.gov](https://www.fueleconomy.gov)
