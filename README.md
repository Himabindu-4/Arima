# README.md

# Household Power Consumption Forecasting Using Exponential Smoothing and ARIMA

## Project Overview

This project focuses on forecasting household electricity consumption using classical time series forecasting techniques. The analysis is performed on the **UCI Individual Household Electric Power Consumption Dataset (2006–2010)** and applies **Exponential Smoothing** and **ARIMA(1,1,1)** models to predict future power consumption patterns.

The study includes data preprocessing, trend analysis, stationarity testing, seasonal decomposition, forecasting, and performance evaluation using standard accuracy metrics.  

---

## Problem Statement

How has daily household global active power consumption varied from 2006 to 2010, what trend and seasonal patterns are present, and can statistical models such as Exponential Smoothing and ARIMA accurately forecast future consumption with measurable accuracy? 

---

## Objectives

* Load and preprocess household power consumption data.
* Handle missing values and datetime conversion.
* Aggregate minute-level observations into daily averages.
* Analyze trends using moving averages.
* Perform seasonal decomposition.
* Test stationarity using the Augmented Dickey-Fuller (ADF) test.
* Build Exponential Smoothing and ARIMA forecasting models.
* Evaluate forecasting performance using MAE and RMSE. 

---

## Dataset Information

| Attribute          | Details                                         |
| ------------------ | ----------------------------------------------- |
| Dataset Name       | Individual Household Electric Power Consumption |
| Source             | UCI Machine Learning Repository                 |
| Date Range         | December 2006 – November 2010                   |
| Records            | ~2,075,259 minute-level observations            |
| Aggregated Records | ~1,433 daily observations                       |
| Main Feature       | Global_active_power                             |
| Missing Values     | Encoded as '?'                                  |



---

## Project Workflow

### 1. Data Collection

* Download dataset from UCI Repository.
* Load dataset into Python environment.
* Extract required columns.
* Convert date and time into a unified datetime format.

### 2. Data Preprocessing

* Handle missing values.
* Convert power consumption values to numeric format.
* Set datetime index.
* Resample data into daily averages.

### 3. Exploratory Analysis

* Time series visualization.
* Moving Average (7-day and 30-day).
* Trend identification.
* Seasonal decomposition.

### 4. Stationarity Analysis

* Augmented Dickey-Fuller (ADF) Test.
* First-order differencing.

### 5. Forecasting Models

* Exponential Smoothing (Additive Trend)
* ARIMA(1,1,1)

### 6. Performance Evaluation

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)

 

---

## Mathematical Techniques Used

### Additive Decomposition

Y(t)=T(t)+S(t)+I(t)

Where:

* **T(t)** = Trend Component
* **S(t)** = Seasonal Component
* **I(t)** = Irregular Component

### Moving Average

CMA(t)=\frac{1}{m}\sum Y(t+k)

Used for smoothing fluctuations and identifying trends.

### Forecast Accuracy Metrics

**MAE (Mean Absolute Error)**

MAE=\frac{1}{n}\sum |Y_t-\hat{Y}_t|

**RMSE (Root Mean Squared Error)**

RMSE=\sqrt{\frac{1}{n}\sum (Y_t-\hat{Y}_t)^2}



---

## Technologies Used

* Python 3.x
* Google Colab
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Statsmodels
* Scikit-learn



---

## Results

### Exponential Smoothing

* Produces smooth and stable forecasts.
* Captures overall trends effectively.
* Suitable for short-term forecasting.

### ARIMA(1,1,1)

* Captures temporal dependencies and autocorrelation.
* Provides more adaptive predictions.
* Achieves better forecasting accuracy than Exponential Smoothing.

### Model Comparison

* Both models generate reliable forecasts.
* ARIMA performs slightly better due to its ability to model time-dependent patterns.

 

---

## Key Findings

* Daily power consumption exhibits trend and seasonal patterns.
* Moving averages effectively reveal long-term consumption behavior.
* Differencing successfully makes the series stationary.
* ARIMA(1,1,1) outperforms Exponential Smoothing in forecasting accuracy.
* Forecasts can support energy planning and demand management.



---

## Limitations

* Daily aggregation removes intra-day consumption patterns.
* Weather and occupancy variables are not included.
* Results are based on a single household.
* ARIMA assumes linear relationships.
* Seasonal effects are not explicitly modeled in ARIMA(1,1,1).



---

## Future Enhancements

* SARIMA for seasonal forecasting.
* SARIMAX with weather variables.
* Facebook Prophet implementation.
* LSTM and Transformer-based forecasting models.
* Multi-household analysis.
* Real-time forecasting systems.



---

## Contributors

| Name        | USN        | Contribution                                                 |
| ----------- | ---------- | ------------------------------------------------------------ |
| Hima Bindu  | 23BTRCL228 | Problem Statement, Documentation, Literature Review          |

---

## References

* UCI Machine Learning Repository – Individual Household Electric Power Consumption Dataset
* Hyndman & Athanasopoulos – Forecasting: Principles and Practice
* Box, Jenkins, Reinsel & Ljung – Time Series Analysis
* Statsmodels Documentation
* Scikit-Learn Documentation



---

### Author

**Hima Bindu (23BTRCL228)**
B.Tech – Artificial Intelligence and Machine Learning
JAIN (Deemed-to-be University)
