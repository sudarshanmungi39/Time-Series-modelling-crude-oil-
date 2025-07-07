# Oil Price Time Series Forecasting

A time series analysis of daily oil prices using ARIMA and LSTM models. The project includes forecasting 24 months into the future and comparing predictions to real Brent prices.

## Table of Contents
- [Overview](#overview)
- [Data Source](#data-source)
- [Methods Used](#methods-used)
- [Results](#results)
- [Comparison](#comparison)
- [Future Improvements](#future-improvements)

## Overview
This project models oil price trends using:
- ARIMA: for traditional linear modeling
- LSTM: for capturing complex temporal patterns

## Data Source
- Assignment dataset: `oil_prices.csv` (July 2020 – Dec 2022)[EIA.gov](https://www.eia.gov/)
- Real Brent Prices: Scraped from [Investing.com](https://www.investing.com/) 

## Methods Used
- ARIMA(p, d, q) parameter tuning with AIC
- LSTM neural network with early stopping
- RMSE and MAE used for evaluation

## Results
### ARIMA:
- Best model: ARIMA(6,1,7)
- RMSE: 2.87 (historical), ~9.11 (real Brent)

### LSTM:
- RMSE: 3.62 (test), ~7.88 (real Brent)
- MAE: 2.91 (test), ~6.46 (real Brent)

## Comparison
| Metric      | ARIMA     | LSTM      |
| ----------- | --------- | --------- |
| RMSE        | 2.87      | 3.62      |
| MAE         | 2.15      | 2.91      |
| Brent RMSE  | ~9.11     | ~7.88     |
| Brent MAE   | ~7.82     | ~6.46     |


## Future Improvements
- Try hybrid ARIMA-LSTM models
- Use exogenous features (e.g., inflation, war index)
- Apply transformer-based forecasting models

## License
This project is licensed under the MIT License.
