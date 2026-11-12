# Used Car Price Prediction

A supervised regression project for estimating used-car selling prices from vehicle age, mileage, engine specifications and categorical vehicle attributes.

## Dataset

- File: `cars.csv`
- Target: `selling_price`
- The script removes duplicate rows, validates positive target prices and parses numeric values embedded in text fields.
- Categorical and numeric preprocessing is fitted inside scikit-learn pipelines.

Check the dataset source, currency/price units and license before redistribution.

## Setup

Python 3.10+:

```bash
python -m venv .venv
# Windows PowerShell: .venv\Scripts\Activate.ps1
# macOS/Linux: source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python train.py
```

## Methodology

The maintained script splits data into training, validation and final test partitions. Candidate models are compared on validation MAE; the selected model is refit on the full training partition and evaluated on the held-out test set. The output includes MAE, RMSE, R² and percentage-within-error bands.

Generated files:
- `cars_model_comparison.csv`
- `cars_test_predictions.csv`

## Limitations

Used-car prices depend on geography, currency, listing date, vehicle condition, accident history and market changes. The dataset may not represent current local prices. Report dataset provenance, units, split strategy and measured metrics when sharing results; do not present a single split as a guarantee.

## License

No license is declared. All rights reserved unless the repository owner adds an explicit license.
