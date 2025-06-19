# Unsupervised Clustering for TBI Readmission Prediction

This repository contains code and notebook material for a study that used an unsupervised approach to stratify traumatic brain injury (TBI) patients by readmission and mortality risk. The work builds on a research manuscript describing how clustering techniques can reveal subgroups of patients with different outcomes.

## Study Overview

The notebook `TBI_FullHouse_3Clusters.ipynb` performs data preprocessing, clustering and predictive modeling. A cohort of TBI patients is imported from `updated_dataset (1).csv`. Continuous and categorical features are cleaned and standardized before applying **k-means** clustering. The resulting clusters are subsequently used to train an **XGBoost** classifier that predicts 30‑day readmission and mortality. Additional visualisations (see `newplot.png`) compare cluster characteristics and highlight clinically relevant variables.

The approach is fully unsupervised for the initial clustering step. Patients are grouped without regard to outcomes, allowing the notebook to identify data‑driven patterns. After cluster assignment, supervised models evaluate whether those groups help differentiate readmission risk. The accompanying manuscript text gives further background on the dataset and details the motivation for using unsupervised learning in this setting.

## Requirements

The analysis relies on standard scientific Python packages. Install them with `pip` if they are not already available:

- `pandas`
- `scikit-learn`
- `xgboost`
- `matplotlib`
- `seaborn`

A local copy of **`updated_dataset (1).csv`** is required. Place this file in the repository directory so the notebook can load it.

## Usage

1. Launch JupyterLab or Jupyter Notebook in this directory.
2. Open `TBI_FullHouse_3Clusters.ipynb`.
3. Run each cell sequentially to reproduce the preprocessing, clustering and prediction steps.
4. Consult the in‑notebook commentary and the manuscript text for interpretation of the results.

## License

This project is released under the [MIT License](LICENSE).
