# Used Car Price Prediction

An educational machine-learning project for predicting used-car prices. The repository contains `cars.csv` and a folder named `used cars 12`; inspect that folder to find the actual model code and confirm the dataset schema and target column.

## Setup

1. Clone or download the repository.
2. Review the dataset source, license, column names, and price units.
3. Inspect `used cars 12` for the training entry point and expected input path.
4. Create a Python virtual environment and install the dependencies required by the source. No root `requirements.txt` is currently listed.
5. Run the documented script or notebook command once confirmed from the project files.

The project description mentions data cleaning, missing-value handling, feature engineering, categorical encoding, and comparisons among regression models. These methods should be verified against the checked-in source. Any previously stated R² value is a project claim, not independently reproduced here.

## Evaluation and privacy

Compare with a baseline using a held-out split; fit encoding and imputation on training data only. Document data provenance, units, split strategy, and metrics. Do not include personal or licensed data without permission. No root test command is currently documented.


## Reproducible run

The training script is the extensionless root file `used cars 12`; run it from the repository root so it can find `cars.csv`.

```bash
python -m venv .venv
# Activate the environment, then:
python -m pip install --upgrade pip
pip install -r requirements.txt
python "used cars 12"
```

The script writes `cars_model_comparison.csv` and `cars_test_predictions.csv` in the current working directory. It selects the model using validation MAE and evaluates the selected model on a separate test split. The checked-in source should be run to reproduce the metrics; no result is guaranteed by the README.
