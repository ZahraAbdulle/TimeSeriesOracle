# TimeSeriesOracle

A powerful time series prediction framework implementing both classical statistical (ARIMA) and deep learning (LSTM) approaches for forecasting stock prices and patient admission rates.

## Description

TimeSeriesOracle provides a flexible and user-friendly implementation of time series forecasting models. The project includes both traditional statistical methods (ARIMA) and advanced deep learning approaches (LSTM) to provide robust predictions for financial markets and healthcare capacity planning.

## Features

- **Dual Model Support**: Compare ARIMA and LSTM predictions side-by-side
- **Flexible Data Sources**: 
  - Real stock market data via Yahoo Finance API
  - Synthetic patient admission data with customizable seasonality and trends
- **Interactive Interface**: Simple command-line prompts for model configuration
- **Visualization**: Automatic plotting of predictions against actual values
- **Performance Metrics**: Mean Squared Error (MSE) calculation for model evaluation

## Installation

This project is designed to run in Google Colab but can be adapted for local environments.

```bash
# Clone the repository
git clone https://github.com/yourusername/TimeSeriesOracle.git
cd TimeSeriesOracle

# Install dependencies
pip install yfinance statsmodels tensorflow sklearn pandas numpy matplotlib
```

## Usage

### In Google Colab

1. Upload the Python script to Colab
2. Install the required dependencies:
   ```python
   !pip install yfinance statsmodels tensorflow sklearn pandas numpy matplotlib
   ```
3. Run the script and follow the prompts:
   ```python
   %run time_series_prediction.py
   ```

### Example Output

When prompted, enter:
- `stock` for stock price prediction, then enter a ticker symbol (e.g., AAPL, MSFT, GOOGL)
- `admission` for patient admission rate prediction (uses synthetic data)

The script will:
1. Fetch or generate appropriate data
2. Split into training and testing sets
3. Train both ARIMA and LSTM models
4. Generate predictions for the test period
5. Calculate Mean Squared Error for each model
6. Plot original data and predictions

## Customization

The code is designed to be easily customizable:
- Adjust training parameters in the function calls
- Modify LSTM architecture in the `lstm_prediction` function
- Change ARIMA order parameters in the `arima_prediction` function
- Adjust the train/test split ratio in the `prepare_data` function

## License

MIT License

## Acknowledgments

- Yahoo Finance API for stock data
- TensorFlow and Keras for deep learning implementation
- StatsModels for ARIMA implementation
