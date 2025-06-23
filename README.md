# Number-of-Corners-prediction

This project tackles the problem of **predicting the total number of corners in a football match** using historical match data and advanced regression techniques. The goal is to build an accurate model for forecasting corner counts, which can be valuable in sports analytics and betting strategy design.

---

##  Objective

Predict the **total number of corners** in a football match based on features like date, team stats, and past match information. The final model is trained using **XGBoost** regression with time series cross-validation.

---

## Data Description

###  Input Datasets:
- `train__1_.xlsx`: Historical match data with home/away corner stats.
- `test__1_.xlsx`: Match data for prediction submission.

###  Key Features:
- `Date`: Match date
- `Home_Corners`, `Away_Corners`: Number of corners for each team
- Derived feature: `Total_Corners` (target variable)

---

##  Modeling Approach

###  Feature Engineering:
- Date parsing and formatting
- Total corners = `Home_Corners` + `Away_Corners`

###  Model Training:
- **Model**: XGBoost Regressor
- **Validation**: TimeSeriesSplit to respect chronological order
- **Metrics**: RMSE (Root Mean Squared Error), MAE (Mean Absolute Error)

### Hyperparameter Tuning:
- Performed via `GridSearchCV` over a time-series split

---

## Evaluation Metrics

The model is evaluated on:
- **RMSE**: Penalizes large errors
- **MAE**: Average magnitude of errors
- Comparison of predictions vs actual values

---

## Libraries Used

- `pandas`, `numpy` – data processing
- `matplotlib`, `seaborn` – visualization
- `xgboost` – modeling
- `scikit-learn` – training, validation, metrics
- `statsmodels`, `scipy` – optional distribution analysis

---
