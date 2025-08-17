# Temperature Forecasting Using Time Series and Machine Learning

### Overview
This project explores temperature forecasting across U.S. cities using time series modeling, ensemble methods, and deep learning. By blending statistical interpretability with machine learning power, it highlights how feature engineering and model diversity can improve climate analytics.

### Dataset
Source: NOAA U.S. daily temperature records (1995–2019).
Size: ~3 million rows.
Variables: Date, location, min/max/avg temperatures.

### Methodology
1. Preprocessing & Feature Engineering
- Lag features, rolling averages, seasonal indicators
- Geographic encodings (latitude, longitude)
2.Modeling Approaches
- ARIMA / SARIMA → statistical baselines for seasonality
- Random Forest → stable ensemble benchmark
- XGBoost → high-accuracy gradient boosting
- LSTM → deep learning for long-term dependencies
3. Evaluation Metrics
- RMSE, MAE, R² for predictive accuracy
4. Visualization
- Interactive dashboards comparing city-level forecasts
- Error distributions and seasonal trend plots

### Results
#### 1. ARIMA / SARIMA (Statistical Baselines)
- Captured seasonal cycles and trends effectively, confirming the yearly temperature oscillations.
- Performance was solid for short-term predictions, but models struggled with extreme temperature anomalies and sudden shifts.
- Their interpretability made them useful for validating feature engineering decisions.

#### 2. Random Forest
- Delivered consistent performance across cities without heavy parameter tuning.
- Handled non-linear relationships better than ARIMA but tended to underestimate peak highs and lows.
- Best used as a stable reference benchmark with low variance.

#### 3. XGBoost
- Top-performing model overall on RMSE and MAE.
- Excelled at learning from engineered lag features and seasonal indicators, capturing both short-term fluctuations and long-term cycles.
- Outperformed Random Forest in predictive sharpness while being faster to train than LSTMs.

#### 4. LSTM (Deep Learning)
- Strong at learning long-term temporal dependencies and complex sequences.
- Performed particularly well on multi-step forecasts where trend continuity mattered.
- However, it required careful hyperparameter tuning and more computational resources to avoid overfitting.

### Conclusion
The project demonstrates that ensemble and deep learning models outperform classical statistical approaches for large-scale temperature forecasting. By combining engineered temporal features with XGBoost and LSTM, forecasts become more accurate and generalizable. These methods can aid climate monitoring, agricultural planning, and energy demand forecasting.
