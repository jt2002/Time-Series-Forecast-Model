# Time Series Forecast Model
Create a SARIMAX Model with Exogeneous Variables to predict energy production

## Data
The data has 5 columns:
1. datetime in 5 mins interval
2. irradiance
3. humidity
4. temperature
5. energy production

## Data Preprocessing
1. Set datetime to index
2. Handle missing values with front filling
3. Handle outliers with Capping and Flooring

## Data Analysis
1. Dickey-Fuller Test for stationarity
2. Seasonality and Trend analysis
3. Auto Correlation Function (ACF)
4. Parial Auto Correlation Function (PACF)
5. Cointegration Test
6. Correlation
7. Quantile-Quantile Plot (QQ Plot)

## Forecast Model of energy production
1. SARIMAX(1, 1, 2)x(2, 0, 2, 12) without exogeneous variables
2. SARIMAX(1, 1, 2)x(2, 0, 2, 12) with exogeneous variables = irradiance, humidity, and temperature

## Key Findings
1. SARIMAX model with exogeneous variables yields better forecasts
2. The predictions well follow seasonality
3. The peaks of the predictions can move up-and-down over time
4. The predictions can follow the low peaks of test data and the flat values that were imputed for missing values

## Caveats
1. Due to the limitation of computing power of my hardware, we resampled the data from 5-min frequency to 2-hours frequency.  As a result, the granularity of our predictions will be 2 hours
2. While SARIMAX model with exogeneous variables is a superior model, when predicting the future, we need to know the future exogeneous information (or at least have confident estimations for it based on some other data)


