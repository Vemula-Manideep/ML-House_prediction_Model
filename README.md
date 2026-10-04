# House Price Prediction — Linear Regression From Scratch

## Project Overview

This project implements an end-to-end house price prediction system using the Kaggle House Prices dataset.

The primary objective is to understand and implement the complete machine learning workflow rather than simply calling a pre-built regression model.

The Linear Regression algorithm is implemented from scratch using NumPy.

## Problem Statement

Predict the sale price of residential properties based on features such as:

* Overall house quality
* Living area
* Basement area
* Garage characteristics
* Number of bathrooms
* Year built
* Remodeling information
* Neighborhood
* Overall property characteristics

## Dataset

Dataset:

Kaggle House Prices — Advanced Regression Techniques

The dataset contains:

* 1,460 training rows
* 81 columns
* Numerical and categorical features

The Kaggle dataset is not included in this repository.

## Machine Learning Pipeline

```text
Raw Kaggle Dataset
        ↓
Exploratory Data Analysis
        ↓
Missing Value Analysis
        ↓
Feature Type Identification
        ↓
Missing Value Handling
        ↓
Categorical Encoding
        ↓
Feature Scaling
        ↓
Linear Regression From Scratch
        ↓
Cross Validation
        ↓
Feature Engineering
        ↓
Hyperparameter Tuning
        ↓
Error Analysis
        ↓
Final Prediction
```

## Linear Regression From Scratch

The model uses the linear regression equation:

```text
y = Xw + b
```

The model parameters are optimized using gradient descent.

The implementation includes:

* Weight initialization
* Prediction
* Mean Squared Error
* Gradient calculation
* Parameter updates
* Training loop
* Prediction

## Feature Engineering

The project includes domain-specific features such as:

* Total square footage
* House age
* Remodeling age
* Total bathrooms
* Total porch area
* Total finished basement area
* Total above-ground area
* Overall quality × living area
* Overall quality × total square footage

## Data Leakage Prevention

The preprocessing pipeline is fitted only on the training portion of each cross-validation fold.

```text
Training Fold
     ↓
Fit Imputer
     ↓
Fit Encoder
     ↓
Fit Scaler
     ↓
Transform Validation Fold
```

This prevents information from the validation data leaking into the training process.

## Evaluation Metrics

The model is evaluated using:

* MAE
* MSE
* RMSE
* R²

Cross-validation is used to obtain a more reliable estimate of model performance.

## Model Results

Current leakage-free cross-validation results:

```text
Mean MAE  : $18,354.35
Mean RMSE : $34,247.20
Mean R²   : 0.7923
RMSE Std  : $9,567.36
R² Std    : 0.1502
```

These values are used as the baseline for subsequent feature-engineering and model-improvement experiments.

## Technologies

* Python
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* Jupyter Notebook
* Kaggle

## Repository Structure

```text
house-price-linear-regression-from-scratch/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── house_price_linear_regression.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── features.py
│   ├── linear_regression.py
│   ├── metrics.py
│   └── train.py
│
├── models/
│   └── README.md
│
├── reports/
│   ├── figures/
│   └── model_results.md
│
└── data/
    └── README.md
```

## Future Improvements

Planned improvements include:

* Residual analysis
* Log transformation of the target
* Outlier handling
* Additional feature selection
* Ridge and Lasso comparison
* Model explainability
* FastAPI inference service
* Dockerization
* Automated testing
* CI/CD
* Cloud deployment

## Learning Objectives

This project demonstrates understanding of:

* Linear regression mathematics
* Gradient descent
* Loss functions
* Feature engineering
* Data preprocessing
* Missing-value handling
* Categorical encoding
* Feature scaling
* Cross-validation
* Data leakage prevention
* Model evaluation
* Error analysis
* ML project organization
