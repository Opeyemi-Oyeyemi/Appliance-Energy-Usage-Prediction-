# Appliance Energy Usage Prediction

Regression analysis to predict household appliance energy consumption
from environmental sensor data.

## Problem
Understanding what drives household energy use is critical for energy
efficiency planning and smart home optimisation. This project models the
relationship between environmental conditions (temperature, humidity, time)
and appliance energy consumption in a low-energy Belgian house.

## Dataset
- Source: UCI Machine Learning Repository (energydata_complete)
- 19,735 observations, 28 features
- Target: Appliances energy use (Wh)
- Features: Temperature/humidity from 9 room sensors + outdoor weather data

## Approach
1. Exploratory analysis and null checks
2. Baseline correlation between temperature sensors
3. Train/test split (70/30) with MinMax scaling
4. Model comparison: Linear Regression · Ridge (L2) · Lasso (L1)
5. Evaluation: MAE · RMSE · R² on train and test sets
6. Overfitting analysis and feature selection via Lasso

## Results
| Model | MAE | RMSE | R² |
|-------|-----|------|-----|
| Linear Regression | 53.643 | 93.64 | 0.149 |
| Ridge | 53.572 | 93.709 | 0.148 |
| Lasso | 58.354 | 99.424 | 0.041 | 

**Key finding:** Lasso regularisation reduced the effective feature set while
maintaining comparable predictive accuracy, suggesting several sensor readings
are redundant for predicting appliance energy use.

## Tools
Python · Pandas · NumPy · Scikit-learn · Matplotlib

## Related
This project connects to my Hamoye ML: Regression certification
(Predicting Energy Efficiency of Buildings, Grade: 84%)
