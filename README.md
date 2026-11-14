# Used Vehicle Price Prediction

> A complete regression workflow for estimating second-hand vehicle prices from structured vehicle specifications.

## Overview
This project studies how vehicle characteristics influence resale value and builds a supervised regression pipeline to estimate a vehicle's selling price. It is designed as an end-to-end tabular ML experiment: raw data inspection, cleaning, feature conversion, preprocessing, model comparison, and final evaluation on held-out data.

## What it does
- Loads the vehicle dataset from `cars.csv`.
- Removes duplicate records and invalid or missing target values.
- Converts numeric-looking text fields such as year, mileage, engine capacity, power, kilometres driven, and seat count into numeric values.
- Separates the selling-price target from input features.
- Splits data into training, validation, and test partitions.
- Detects numerical and categorical columns and builds preprocessing pipelines.
- Imputes missing numeric values with medians and categorical values with the most frequent value.
- Applies scaling to numerical inputs and one-hot encoding to categorical features.
- Compares Linear Regression, Ridge, Decision Tree, Random Forest, Extra Trees, and Gradient Boosting variants.
- Reports MAE, RMSE, R², and the percentage of predictions within selected error bands.
- Selects a model using validation results, retrains it on the training-plus-validation data, and evaluates it on the held-out test set.

## Model evaluation
The script ranks candidates by validation MAE and prints final test metrics. The repository description has previously reported an approximate R² of 0.81; treat that as a project-reported result, not a guarantee for other data or a result independently reproduced by this README.

## Repository contents
- `cars.csv` — vehicle dataset used by the experiment.
- `used cars 12` — Python training script (filename intentionally contains a space and has no extension).

## Requirements
Python 3.10+ is recommended. Install:
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate
python -m pip install --upgrade pip
pip install pandas numpy scikit-learn
```

## Run
Run from the repository root so the relative dataset path resolves:
```bash
python "used cars 12"
```
The script prints the model comparison and final test metrics, and writes `cars_model_comparison.csv`.

## Reproducibility notes
The split uses a fixed random seed. Results can still vary with library versions and dataset changes. The model is a research/learning tool, not a vehicle appraisal or a substitute for inspection, market comparisons, or professional valuation. Confirm dataset provenance, currency, and price units before interpreting predictions.

## Skills demonstrated
Tabular data cleaning · Feature preprocessing · Regression · Scikit-learn Pipelines · Model selection · Validation strategy · Error analysis
