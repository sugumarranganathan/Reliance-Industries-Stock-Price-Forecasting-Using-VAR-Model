# Reliance-Industries-Stock-Price-Forecasting-Using-VAR-Model

https://colab.research.google.com/drive/1AiU7KpUlevHJ3MJRYjl3FMPBUBHuTgag#scrollTo=681tnkW1UKX5


## Project Overview

This project focuses on forecasting Reliance Industries stock prices using the Vector Autoregression (VAR) model. The analysis utilizes historical stock market data, including Open, High, Low, Close, and Volume variables, to capture interdependencies among multiple time series and predict future stock movements.

---

## Objectives

* Analyze historical stock price behavior of Reliance Industries.
* Test stationarity of stock market variables.
* Apply differencing to achieve stationarity.
* Build a Vector Autoregression (VAR) model.
* Forecast future stock prices for the next 7 trading days.
* Visualize and interpret forecasting results.

---

## Dataset Information

| Attribute   | Description                    |
| ----------- | ------------------------------ |
| Company     | Reliance Industries Ltd.       |
| Data Source | Yahoo Finance                  |
| Period      | 2023 – 2025                    |
| Variables   | Open, High, Low, Close, Volume |
| Frequency   | Daily Stock Data               |

---

## Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Statsmodels
* Scikit-Learn

---

## Methodology

### 1. Data Collection

Historical stock price data was collected and loaded into a Pandas DataFrame.

### 2. Data Preprocessing

* Date conversion and indexing
* Missing value verification
* Variable selection

### 3. Stationarity Testing

The Augmented Dickey-Fuller (ADF) test was applied to all variables.

#### Initial ADF Test Result

| Variable | Result         |
| -------- | -------------- |
| Open     | Non-Stationary |
| High     | Non-Stationary |
| Low      | Non-Stationary |
| Close    | Non-Stationary |
| Volume   | Stationary     |

### 4. First-Order Differencing

Differencing was applied to remove trends and achieve stationarity.

#### Final ADF Test Result

| Variable | Result     |
| -------- | ---------- |
| Open     | Stationary |
| High     | Stationary |
| Low      | Stationary |
| Close    | Stationary |
| Volume   | Stationary |

### 5. Lag Selection

Optimal lag order was selected using information criteria.

| Criterion | Selected Lag |
| --------- | ------------ |
| AIC       | 15           |
| FPE       | 15           |
| HQIC      | 15           |
| BIC       | 10           |

Final Model Selected: **VAR(15)**

### 6. Model Training

The VAR(15) model was trained using the stationary differenced dataset.

### 7. Forecasting

Future stock prices were forecasted for the next 7 trading days.

---

## Forecast Results

### Predicted Stock Prices

| Day   |    Open |    High |     Low |   Close |
| ----- | ------: | ------: | ------: | ------: |
| Day 1 | 1198.18 | 1208.12 | 1188.36 | 1199.46 |
| Day 2 | 1200.06 | 1209.98 | 1189.94 | 1200.36 |
| Day 3 | 1199.46 | 1211.19 | 1189.54 | 1200.84 |
| Day 4 | 1200.03 | 1211.15 | 1189.84 | 1201.53 |
| Day 5 | 1199.69 | 1211.19 | 1191.35 | 1201.53 |
| Day 6 | 1200.64 | 1212.41 | 1193.38 | 1203.10 |
| Day 7 | 1202.66 | 1214.13 | 1195.99 | 1206.08 |

---

## Forecast Interpretation

* Forecasted closing price increased from **1199.46** to **1206.08**.
* Expected gain: **+6.62 points**.
* The model indicates a gradual upward trend.
* No significant volatility is observed during the forecast horizon.
* Reliance Industries exhibits stable short-term growth potential.

---

## Results Summary

| Parameter           | Result       |
| ------------------- | ------------ |
| Model Used          | VAR(15)      |
| Forecast Horizon    | 7 Days       |
| Predicted Trend     | Upward       |
| Initial Close Price | 1199.46      |
| Final Close Price   | 1206.08      |
| Net Change          | +6.62 Points |
| Market Outlook      | Positive     |

---

## Conclusion

The VAR(15) model successfully captured the dynamic relationships among Open, High, Low, Close, 
and Volume variables of Reliance Industries stock data. After achieving stationarity through first-order differencing, 
the model generated reliable short-term forecasts. The results indicate a gradual increase in stock prices over
the next seven trading days, suggesting a positive short-term market outlook. 
This study demonstrates the effectiveness of multivariate time-series forecasting using the Vector Autoregression approach.

---

## Future Enhancements

* Compare VAR with ARIMA, SARIMA, and LSTM models.
* Perform rolling forecast validation.
* Include macroeconomic indicators as external variables.
* Develop a real-time stock forecasting dashboard.
* Evaluate model performance using MAE, RMSE, and MAPE metrics.

---

## Prepared by

**Sugumar Ranganathan, M.B.A.,**


