# Geospatial Rental Analysis

A Python project exploring how location and proximity to amenities relate to rental prices around La Jolla Village and University City in San Diego.

The project combines geospatial feature engineering, regression modeling, and an exploration of conformal prediction intervals to analyze median rent per square foot.

## Approach

- Build location-based features describing proximity to beaches, shopping, downtown, schools, parks, and transit.
- Compare regression models using different feature combinations and both original and log-transformed rental prices.
- Use AIC and BIC for model selection and explore prediction uncertainty with conformal prediction.

## Repository Structure

| File | Description |
| --- | --- |
| `data_build(2).ipynb` | Geospatial data preparation and feature engineering. |
| `full_rent_features.csv` | Prepared rental dataset and location-based features. |
| `model.ipynb` | Regression analysis and model diagnostics. |
| `regression_with_conformal.ipynb` | Regression modeling with calibration-based prediction intervals. |

## Getting Started

Clone the repository:

```bash
git clone https://github.com/choi8616/geospatial-rental-analysis.git
cd geospatial-rental-analysis
```

Install the packages used by the modeling notebooks:

```bash
python -m pip install notebook pandas numpy matplotlib statsmodels scikit-learn
```

Launch Jupyter:

```bash
jupyter notebook
```

Open `model.ipynb` or `regression_with_conformal.ipynb` and run the cells in order. Keep `full_rent_features.csv` in the same directory as the notebooks.

## Data Preparation

The modeling notebooks use the included CSV, so rebuilding the dataset is optional.

Running `data_build(2).ipynb` requires additional geospatial packages, including GeoPandas, Shapely, and OSMnx, along with the external geospatial files and intermediate CSVs referenced in the notebook. Those additional data inputs are not included in this repository.

## Scope

This is an exploratory analysis, not a production rental-pricing system. The models examine associations between location and rental prices rather than establishing causal effects.
