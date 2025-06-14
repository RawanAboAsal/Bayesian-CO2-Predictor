# CO2 Emission Prediction using Regression Analysis

## Project Overview
This project focuses on predicting **CO2 emissions** using both **Bayesian** and **Classical** regression techniques. It aims to compare their performance and identify the most suitable model for accurate and robust emission prediction.

## Table of Contents
- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Methodology](#-methodology)
  - [Data Preprocessing and EDA](#-data-preprocessing-and-eda)
  - [Feature Engineering and Scaling](#-feature-engineering-and-scaling)
  - [Model Training and Evaluation](#-model-training-and-evaluation)
- [Models Implemented](#-models-implemented)
  - [Bayesian Linear Regression](#-bayesian-linear-regression)
  - [Classical Linear Regression](#-classical-linear-regression)
- [Results and Discussion](#-results-and-discussion)


##  Dataset
The dataset used is `CO2 Emission.csv`, which includes various environmental features used to predict the `emission` target variable.

### Features:
- `latitude`, `longitude`
- `SulphurDioxide_*`, `CarbonMonoxide_*`, `NitrogenDioxide_*`, `Ozone_*`
- `Cloud_*`, `CarbonMonoxide_cloud_height`, etc.

### Target:
- `emission`: The amount of CO2 emitted.

---

##  Methodology

###  Data Preprocessing and EDA
- Displayed data structure, types, and missing values.
- Skewness analysis with histograms.
- Power transformation (Yeo-Johnson) to reduce skewness.
- Outlier detection using boxplots and capping via 1.5 IQR.
- Correlation heatmap for multicollinearity analysis.
- Target distribution and feature correlation analysis.

### Feature Engineering and Scaling
- Applied **StandardScaler** to normalize feature values.

###  Model Training and Evaluation
- Dataset split: **80% train**, **20% test**.
- Models trained on training data.
- Predictions made on test set.
- Evaluated using:
  - Mean Squared Error (MSE)
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - R² Score (where applicable)

---

##  Models Implemented

### Bayesian Linear Regression
- Bayesian models with different priors:
  - **Normal**, **Beta**, **Laplace**, **Gamma**
- Tools used: **PyMC**, **ArviZ**
- Analysis included:
  - Trace plots
  - Posterior predictive checks with 95% intervals
  - Statistical summaries
  - Posterior MSE distribution

###  Classical Linear Regression
- Implemented models:
  - Simple Linear Regression
  - Polynomial Regression
  - Ridge Regression (L2)
  - Lasso Regression (L1)
- Evaluated via predicted vs. actual plots and standard metrics.

---

## Results and Discussion
- Bayesian models showed uncertainty quantification via posterior intervals.
- Choice of prior distribution impacted prediction quality.
- Classical regularized models (Ridge, Lasso) helped address multicollinearity.
- Top-performing models highlighted in terms of MSE, MAE, and RMSE.

