
# Statistical Machine Learning Project: Health Insurance Premium Prediction

## Overview
This project builds and compares multiple machine learning models to predict
medical insurance premium prices for individuals based on their health-related
and demographic features. The goal is to identify the best-performing model
in terms of prediction accuracy.

## Dataset Overview:
-Samples: 986 individuals

-Target Variable: PremiumPrice (in ₹ INR, The Indian rupee)

Features Used:
### Demographic Features
-Age: Age of the person

-Height: Height in cm

-Weight: Weight in kg

-NumberOfMajorSurgeries: Total number of past major surgeries
### Medical/Health Features

•	Diabetes: 1 if the person has diabetes, else 0

•	BloodPressureProblems: 1 if yes, else 0

•	AnyTransplants: 1 if any transplant done

•	AnyChronicDiseases: 1 if any chronic illness

•	KnownAllergies: 1 if any known allergies

•	HistoryOfCancerInFamily: 1 if yes, else 0

## Methods & Models
The project covers the full machine learning pipeline:

| Step | Description |
|------|-------------|
| **EDA** | Exploratory Data Analysis — distributions, correlations, outliers |
| **Linear Regression** | Baseline regression model |
| **Regression Tree** | Decision tree for non-linear relationships |
| **Random Forest** | Ensemble method for improved accuracy |
| **Gradient Boosting (GBM)** | Boosting method for high performance |
| **Neural Networks** | Deep learning approach |
| **PCA** | Principal Component Analysis for dimensionality reduction |

•	Data Cleaning & Normalization

•	Principal Component Analysis (PCA)

•	Cross-Validation (CV-RMSE)

•	Model Evaluation & Comparison

•	Final Test on Holdout Set

## Tools & Technologies
- **Language:** R
- **Format:** R Notebook (`.nb.html` / `.Rmd`)

## Results
Model Comparison Based on CV RMSE:

Without PCA, the best model is Random Forest with a CV-RMSE of 3071.27, followed by Regression Tree (3379.69) and GBM (3223.96).

With 8 PCs, all models performed worse in terms of CV-RMSE. The best among them is still Random Forest with a CV RMSE of 4160.99, but this is significantly worse than its performance on original variables.

PCA did not improve model performance for any of the 5 models. It even increased the CV RMSE by over 1000 in most cases.

we conclude that dimensionality reduction via PCA was not beneficial in this project, as the original variables already had strong predictive power and relatively low dimensionality.

The best model is the one with the lowest CV-RMSE, because it best reflects expected performance on future (test) data. Best Model Overall is Random Forest without PCA. It has the lowest CV RMSE (3071.27).
