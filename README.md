# Apple (AAPL) Stock Price Prediction (ARIMA-LSTM)

This project uses a combination of ARIMA (AutoRegressive Integrated Moving Average) and LSTM (Long Short-Term Memory) models to predict future stock prices for Apple Inc. (AAPL). By combining traditional time series forecasting with modern machine learning techniques, the model aims to improve the accuracy of stock price predictions.

The project takes historical stock price data along with financial fundamentals (e.g., earnings, revenues) and applies an ARIMA model to forecast stock prices. The residuals (errors) from the ARIMA model are then passed through an LSTM model, which helps capture complex patterns and trends for better prediction.

### Dataset:
- **`prices-split-adjusted.csv`**: Contains historical adjusted stock prices (daily) for multiple stocks.
- **`fundamentals.csv`**: Contains fundamental data such as earnings, revenues, etc., for multiple stocks.

Both datasets are part of the **NYE Stocks Dataset**, which is used to enhance the prediction process by combining price data with fundamental analysis.

### Project Flow:
1. **Data Preprocessing**: The price and fundamental data are filtered to include only the data for Apple Inc. (AAPL). The datasets are then merged based on the year of the financial reports and stock prices.
2. **ARIMA Model**: The ARIMA model is used to forecast the stock prices based on historical price data. It captures the trends and patterns in the stock prices.
3. **LSTM Model**: The residuals (errors) from the ARIMA model are passed through an LSTM network to capture any additional patterns that ARIMA might not have modeled. The combination of ARIMA and LSTM is used to make more accurate predictions.
4. **Prediction**: The model predicts stock prices for the next 252 business days (approximately 1 year).
5. **Evaluation**: Performance is evaluated using common metrics like MSE (Mean Squared Error), RMSE (Root Mean Squared Error), MAE (Mean Absolute Error), and MAPE (Mean Absolute Percentage Error).
6. **Visualization**: A graph is generated showing the historical stock prices along with the predicted stock prices for the next year.

### Dependencies:
- **pandas**: For data manipulation and merging.
- **scikit-learn**: For preprocessing and scaling the data.
- **statsmodels**: For the ARIMA time series model.
- **tensorflow**: For the LSTM neural network model.
- **numpy**: For numerical operations.
- **matplotlib**: For data visualization.
- **sklearn.metrics**: For evaluation metrics.
