# House Prices - Advanced Regression Techniques

Kaggle competition solution for predicting house sale prices.

**Competition:** [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

---

## Result

| Metric              | Score     |
|---------------------|-----------|
| Local CV (RMSLE)    | ~0.118    |
| Kaggle              | 0.12771

---

## Approach

- Target transformation: log1p(SalePrice) (matches official metric)
- Missing values: Treated "NA" as meaningful category (None)
- Feature Engineering:
  - TotalSF, TotalBath, TotalPorchSF
  - House Age & Remodel Age
  - Binary flags (HasGarage, HasPool, etc.)
  - Ordinal encoding for quality features
- Models: Tuned XGBoost + LightGBM (50/50 blend)
- Validation: 5-Fold Cross-Validation

---

## Project Structure

├── train.csv
├── test.csv
├── data_description.txt
├── submission.csv          # Final predictions
└── README.md
