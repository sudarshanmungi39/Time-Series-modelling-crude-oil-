#  Oil Price Time Series Forecasting

A time series analysis of daily oil prices using **ARIMA** and **LSTM** models. This project forecasts oil prices 24 months ahead and compares them with real Brent crude prices for validation.

---

##  Table of Contents
- Overview  
- Data Source  
- Methods Used  
- Results  
- Comparison  
- Future Improvements  
- License  

---

##  Overview

This project models oil price trends using:

- **ARIMA**: for traditional, interpretable linear modeling  
- **LSTM**: to capture non-linear and dynamic patterns in the data  

The goal is to evaluate each model’s forecasting capability and compare predictions against actual Brent prices from Jan 2023 to Jun 2025.

---

##  Data Source

- `oil_price.csv`: Daily oil prices from **July 2020 – Dec 2022** (provided in assignment)
- Real Brent prices: Retrieved from  
  [EIA.gov](https://www.eia.gov/dnav/pet/pet_pri_spt_s1_d.htm) and Investing.com

---

##  Methods Used

- **ARIMA (6,1,7)** selected using AIC grid search  
- **LSTM**: 2-layer neural network with early stopping, dropout, and 60-day sequence window  
- Forecast length: **730 days (24 months)**  
- Evaluation metrics: **RMSE** and **MAE**  

---

##  Results

###  ARIMA  
- Best model: **ARIMA(6,1,7)**  
- RMSE (test split): **26.12**  
- MAE (test split): **24.09**  
- RMSE (Brent real-world): **5.70**  
- MAE (Brent real-world): **4.69**  

###  LSTM  
- RMSE (direct test): **2.53**  
- MAE (direct test): **1.98**  
- RMSE (forecast vs Brent): **13.50**  
- MAE (forecast vs Brent): **10.67**

---

##  Model Performance Comparison

| Metric            | ARIMA (Test) | ARIMA (Brent) | LSTM (Test) | LSTM (Forecast) |
|-------------------|---------------|----------------|--------------|------------------|
| **RMSE**          | 26.12         | 5.70           | 2.53         | 13.50            |
| **MAE**           | 24.09         | 4.69           | 1.98         | 10.67            |


---

##  Future Improvements

- Try **hybrid ARIMA-LSTM** models  
- Use **exogenous features** (e.g., inflation, geopolitical events)  
- Explore **transformer-based** or attention-based time series models  
- Apply **rolling retraining** for long-term LSTM forecasting  

---

##  License

This project is licensed under the **MIT License**.

