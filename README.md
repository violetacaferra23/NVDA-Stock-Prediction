# NVIDIA Stock Prediction using LSTM

This repository containg a comprehensive analysis of the stock market NVDA data. The analysis covers historical price movements over the past five years, moving averages, bollinger bands, relative strength index (RSI) and moving average convergence/divergence (MACD). Additionally, the repository includes a machine learning model for predictin future stocks prices using LSTM (Long Short-Term Memory) neural networks.

## Table of contents

1. [Data Exploration](#data-exploration)
2. [Stock Price Prediction](#stock-price-prediction)
3. [Hyperparameters](#hyperparameters)
4. [Predictions and results](#predictions-and-results)
5. [Future Work](#future-work)

## Data exploration

### Getting the Data

The stock data is fetched from Yahoo Finance using the `pandas_datareader` and `yfinance` libraries. The dataset includes the adjusted closing prices and trading volume of NVDA from 2019.

### Analysis

1. **Closing prices over time:**
Historical closing prices and volume of sales are visualized to observe trends and patterns.

![Closing_prices.png] https://github.com/violetacaferra23/NVDA-Stock-Prediction/blob/main/Closing_prices.png

The stock price shows a significant upward trend, particularly from 2020 onward. This suggests strong long-term growth, likely driven by NVIDIA's strategic positioning in industries like gaming, AI, and data centers.

The stock shows periods of volatility, particularly in the sharp peaks and dips observed in 2022 and 2023. These fluctuations might reflect the impact of market events or investor sentiment regarding NVIDIA's potential in the tech sector.

2. **Moving averages:**
Moving averages for 20, and 50 days are calculated and plotted to understand the stock trends over different time periods.

![Precio de cierre con 20 y 50 days.png]https://github.com/violetacaferra23/NVDA-Stock-Prediction/blob/main/Precio%20de%20cierre%20con%2020%20y%2050%20days.png

We see in graph that the best values to measure the moving average ir 20 days because we still capture trends in the data without noise.

3. **Bollinger data:**

![bollinger data.png] https://github.com/violetacaferra23/NVDA-Stock-Prediction/blob/main/bollinger%20data.png

Bollinger Bands are a technical analysis tool that plots bands around a moving average. They help identify overbought and oversold conditions, as well as potential trend reversals. Wider bands indicate higher volatility, while narrower bands suggest lower volatility.

4. **Relative strenght index:**

![RSI.png]https://github.com/violetacaferra23/NVDA-Stock-Prediction/blob/main/RSI.png

* High Volatility: The frequent crossings of the overbought and oversold levels indicate significant price swings.
* Upward Trend: The RSI consistently being in the overbought zone suggests a strong upward momentum, especially for growth stocks.
* Trading Opportunities: Crossovers above 70 (overbought) or below 30 (oversold) can signal potential buy or sell opportunities, but should be confirmed with other indicators.

5. **MACD(Moving Average Convergence/Divergence):**

![macd.png]https://github.com/violetacaferra23/NVDA-Stock-Prediction/blob/main/macd.png

* The MACD chart indicates a strong bullish trend for NVIDIA, especially in 2023, as reflected in the price history chart.
* The peaks in the MACD histogram in 2023 and early 2024 show increased momentum, suggesting potential buying opportunities during these times.
* However, the recent fluctuations in the MACD line in late 2024 suggest that the trend could be more volatile moving forward.

## Stock Price Prediction

An LSTM model is used to predict future stock prices. The model is trained using TensorFlow/Keras and configured with specific hyperparameters optimized for stock price prediction.

### Model Architecture

The LSTM model consists of:
1. **LSTM Layers** - Captures the temporal dependencies in stock price data.
2. **Dense Layers** - Produces the final output, which is a predicted stock price.
The model was trained using a mean squared error loss function and the Adam optimizer. The stock price data was normalized before training to improve performance and stability.

## Hyperparameters

The model is configured with the following hyperparameters:

- **Number of LSTM Units**: *e.g., 50, 100* (adjust based on experimentation)
- **Batch Size**: *e.g., 32* (defines the number of samples used for each model update)
- **Learning Rate**: *e.g., 0.001* (controls the step size at each iteration while moving toward a minimum of the loss function)
- **Epochs**: *e.g., 50* (number of complete passes through the training dataset)
- **Dropout Rate**: *e.g., 0.2* (used in LSTM layers to prevent overfitting)

## Prediction Results and Evaluation

The model’s predictions were evaluated using Mean Squared Error (MSE) and Mean Absolute Error (MAE). Here are some example results:

MSE: 0.0004 (example value, adjust based on actual results)
MAE: 0.015 (example value, adjust based on actual results)
These values suggest the model has a reasonable level of accuracy in capturing trends but might have limitations in exact price prediction.

### Sample Prediction Plot

![model lstm and prediction.png]https://github.com/violetacaferra23/NVDA-Stock-Prediction/blob/main/model%20lstm%20and%20prediction.png

*Note: The above plot compares the model's predicted stock prices against actual historical prices. This helps visualize how well the model can follow the stock's trend over time.*

### Results

The model's performance was evaluated using mean squared error (MSE) and mean absolute error (MAE) metrics. Results indicate that the model can reasonably capture trends in stock price movements, though further optimization might improve accuracy.

## Future work


