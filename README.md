# S&P 500 and VIX Anomaly Detection

This project aims to identify outliers and market anomalies using the VIX (CBOE Volatility Index) and the S&P 500 index. The goal is to develop a method for tracking market sentiment that can be applied to specific stocks.

## Project Overview

The project uses machine learning techniques to detect anomalies in financial market data, specifically focusing on the relationship between the S&P 500 index and the VIX. It employs two main anomaly detection algorithms:

1. Isolation Forest
2. Local Outlier Factor (LOF)

After detecting anomalies, the project then uses these anomalies to predict potential price reversals ("flips") in the market.

## Key Features

- Data preprocessing and feature engineering
- Anomaly detection using Isolation Forest and LOF
- Hyperparameter tuning for both anomaly detection models
- Statistical significance testing of detected anomalies
- Prediction of price reversals using Random Forest Classifier
- Visualization of results using various plotting techniques

## Methodology

1. **Data Collection**: The project uses Yahoo Finance API to collect historical data for the S&P 500 index and the VIX.

2. **Feature Engineering**: Several features are created, including high-low price changes, open-close price changes, RSI (Relative Strength Index), DPO (Detrended Price Oscillator), and PSK (Pring's Special K).

3. **Anomaly Detection**: Both Isolation Forest and LOF algorithms are applied to detect anomalies in the dataset.

4. **Hyperparameter Tuning**: Grid search is used to find the optimal parameters for both anomaly detection models.

5. **Statistical Testing**: Binomial tests are conducted to determine if the detected anomalies are statistically significant.

6. **Prediction Model**: A Random Forest Classifier is trained on the detected anomalies to predict whether a price reversal will occur.

7. **Visualization**: Various plots are created to visualize the detected anomalies and the performance of the prediction model.

## Results

The project demonstrates that both anomaly detection methods (Isolation Forest and LOF) can identify statistically significant anomalies in the S&P 500 and VIX data. The subsequent Random Forest Classifier achieves high accuracy (around 95%) in predicting price reversals based on these anomalies.

## Future Work

Potential areas for future development include:
- Applying the methodology to individual stocks
- Incorporating more features or alternative data sources
- Exploring other machine learning algorithms for anomaly detection and prediction
- Developing a real-time anomaly detection and prediction system

## Dependencies

- pandas
- yfinance
- scikit-learn
- numpy
- matplotlib
- seaborn
- plotly

## Usage

To run this project, clone the repository and run the Jupyter notebook. Make sure you have all the required dependencies installed.

```bash
jupyter notebook S&P\ Correlation.ipynb
```

## Disclaimer

This project is for educational purposes only and should not be used for actual trading without further validation and risk management strategies.

## License

[MIT](https://choosealicense.com/licenses/mit/)
