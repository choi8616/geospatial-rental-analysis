# MATH 189 Final Project Submission

Project title: **Rent Analysis On and Off Campus at UC San Diego**

Hi! This folder contains our final report, the dataset used for the analysis, and the notebooks that produced the results discussed in the report.

## What to Look At First

The main analysis notebook is `regression_with_conformal.ipynb`. This is the best place to start if you want to reproduce the final model selection, conformal prediction interval, diagnostics, and UCSD on-campus housing comparison from the report.

The file `full_rent_features.csv` should stay in the same folder as the notebooks, since the modeling code reads it directly from the local directory.

## Files Included

- `final_report.pdf`: our final written report.
- `regression_with_conformal.ipynb`: the main notebook used for the final analysis.
- `model.ipynb`: an earlier regression/model-selection notebook that supports the final workflow.
- `data_build.ipynb`: the notebook used to build the processed rental feature dataset.
- `full_rent_features.csv`: the processed dataset used by the modeling notebooks.
- `requirements.txt`: a short list of Python packages used in the notebooks.

## Suggested Run Order

1. Run `regression_with_conformal.ipynb` first. This reproduces the main statistical analysis from the included processed dataset.
2. Review `model.ipynb` if you want to see the earlier regression/model-selection workflow.
3. Use `data_build.ipynb` as a record of how the dataset was constructed. This notebook may not run from a fresh environment unless the external GIS files, API access, and geospatial packages are also available.

## Data Note

The final analysis uses `full_rent_features.csv`, which is the processed dataset after rental estimates and geospatial distance features were assembled. The data-building process used sources such as SanGIS parcel/land-use files, RentCast rental estimates, and OpenStreetMap amenity data through OSMnx.

Because the final modeling notebooks only need `full_rent_features.csv`, they should be easier to reproduce than the full data-building workflow.
