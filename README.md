# GLD_Vindatathon

## Overview

This repository contains a machine learning pipeline for revenue and cost forecasting. The workflow covers data preprocessing, feature engineering, model training, ensembling, evaluation, and submission generation.

---

## Project Structure

```
GLD_Vindatathon/
│
├── orgdata/              # Raw input data
├── cleandata/            # Processed data (generated)
├── notebooks/
│   ├── 01_preprocess.ipynb
│   └── 02_model.ipynb
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/Cheemshoang/GLD_Vindatathon.git
cd GLD_Vindatathon
pip install -r requirements.txt
```

---

## Usage

### Step 1: Data Preprocessing

Run the preprocessing notebook:

```
notebooks/01_preprocess.ipynb
```

This step generates cleaned and feature-engineered datasets stored in:

```
cleandata/
```

---

### Step 2: Model Training and Prediction

Run the modeling notebook:

```
notebooks/02_model.ipynb
```

This step performs:

- Model training using LightGBM, XGBoost, Ridge Regression and baseline formula model
- Ensemble learning via Voting regressor with L
- Model evaluation using standard regression metrics
- SHAP-based model interpretation

---

## Output

The final submission file is generated at:

```
orgdata/submission.csv
```

---

## Evaluation Metrics

The models are evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

---

## Notes

- Ensure all required raw data files are placed in `orgdata/` before execution
- Notebooks must be executed in sequence (preprocessing before modeling)
- Large data files should not be committed to the repository; use `.gitignore` or external storage if necessary

---
