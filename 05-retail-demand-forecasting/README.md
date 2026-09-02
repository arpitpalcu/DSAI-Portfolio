# Retail Demand Forecasting & Inventory Intelligence

## Business Problem
Retailers need reliable demand estimates to reduce stockouts, avoid excess inventory, and plan replenishment. This project converts transaction-level retail data into a time-aware forecasting workflow and an inventory-risk layer.

## Objectives
- Understand demand trends and seasonality.
- Engineer historical demand signals using lag and rolling features.
- Compare tree-based forecasting models using a chronological holdout set.
- Translate forecast demand into relative inventory-risk categories.

## Workflow
1. Data preparation and validation
2. Exploratory demand analysis
3. Time-based feature engineering
4. Chronological train/test split
5. Random Forest and Gradient Boosting models
6. MAE and RMSE evaluation
7. Actual-vs-predicted analysis
8. Feature-importance analysis
9. Inventory demand-risk interpretation

## Key Features
- Lag demand: 1, 7, 14, and 28 periods
- Rolling mean: 7 and 28 periods
- Rolling standard deviation: 7 and 28 periods
- Promotion rate
- School-holiday rate
- Month, day-of-week, and week-of-year indicators

## Models
- Random Forest Regressor
- HistGradientBoostingRegressor

Models are evaluated on a chronological holdout rather than a random split to reduce temporal leakage.

## Evaluation
The project uses:
- **MAE** — average absolute forecast error.
- **RMSE** — penalizes larger forecast errors more strongly.

The model comparison table and forecast visualization are generated in the notebook.

## Inventory Intelligence
Forecast demand is converted into relative **High / Medium / Low** demand-risk categories using the forecast distribution. This is an analytical prioritization layer, not a direct replacement for operational inventory policy.

## Repository Structure
```text
05-retail-demand-forecasting/
├── data/
├── notebooks/
│   └── 01_retail_demand_forecasting.ipynb
├── outputs/
│   └── figures/
├── .gitignore
├── requirements.txt
└── README.md
```

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_retail_demand_forecasting.ipynb
```

Run the notebook from top to bottom after confirming the input dataset path.

## Limitations & Next Steps
- The current workflow forecasts an aggregated demand series rather than a full product-warehouse hierarchy.
- A naive seasonal baseline should be added before treating the ML models as operationally useful.
- Future improvements should include walk-forward validation, product-level forecasting, intermittent-demand handling, and hyperparameter tuning.

## Portfolio Focus
This project demonstrates time-series-aware feature engineering, regression modeling, model evaluation, and business interpretation for inventory planning.
