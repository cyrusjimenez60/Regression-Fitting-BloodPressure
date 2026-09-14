# Regression Fitting - Blood Pressure

A demonstration on model training to show different kinds of fit (overfit, underfit, best fit) using polynomial regression on a blood pressure dataset.

## Overview

This project explores the concepts of underfitting, overfitting, and ideal (best) fitting through a hands-on regression demonstration. Using a linear regression model provided by CISCO's data science course as a base, the model is extended into polynomial regression of varying degrees to observe how model complexity affects prediction performance and generalization.

All code implementation and execution were performed in Google Colaboratory (Google Colab), removing the need for local package installation.

## About the Dataset

**Does blood pressure increase with age?**

The `blood-pressure-usa.csv` file contains systolic blood pressure readings from 100 individuals sampled by the National Health and Nutrition Examination Survey (NHANES) in the U.S., with each person measured three times (averaged into a single blood pressure value per person for this analysis).

## Methodology

Three polynomial regression models of varying complexity were trained and compared on the dataset:

- **Underfit Model (Degree 1)** — Too simple; represents the relationship as a straight line and misses the subtle curvature in the data, resulting in high bias.
- **Good Fit Model (Degree 4)** — Balanced; captures the overall trend and curvature without excessive fluctuation, achieving the strongest generalization to unseen data.
- **Overfit Model (Degree 20)** — Too complex; closely chases individual data points and noise rather than the true underlying pattern, resulting in high variance and poor performance on test data.

Each model was evaluated using R² and Mean Squared Error (MSE) on both training and testing sets.

## Key Findings

- The **degree-4 (good fit) model** achieved the highest R² values on both training (0.4955) and testing (0.4327) sets, along with the lowest MSE, making it the most reliable model for this dataset.
- The **degree-1 (underfit) model** captured the general upward trend but failed to represent the data's subtle curvature.
- The **degree-20 (overfit) model** performed the worst on unseen data, despite its complexity, due to memorizing noise rather than learning the true pattern.
- Overall, the results confirm that blood pressure does tend to increase with age, though the relationship is gradual and influenced by other factors such as lifestyle, diet, and genetics.

## Documentation
Click the link to view the full project documentation:
[Model_Fitting_Documentation.pdf](Model_Fitting_Documentation.pdf)
