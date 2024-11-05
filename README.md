NVIDIA Stock Prediction using LSTM

NVIDIA's stock price is predicted over -some months- using an Long Short-Term Memory (LSTM) Machine Learning's model. The analysis covers historical price movements and sentiments data with Tweets about NVIDIA to improve prediction accuracy.

First, the stock price is predicted over some months using an LSTM Multivariate Time-Series Prediction model. Then, tweets about NVIDIA are cleaned and their daily average sentiment scores are computed using TextBlob. Lastly, the daily average sentiment scores are added as a feature in the LSTM model and used for prediction.

A model solely dedicated to predicting NVIDIA's stock price can benefit from excluding macroeconomic factors under certain conditions:
* Stock-specific focus: The primary goal is to identify and capitalize on NVIDIA's unique trends, a simpler model focused on stock-specific data can be more effective.
* LSTM complexity management: Given the LSTM's complex architecture, incoporating numerous macroeconomic variables can introduce noise.
* Limited macoeconomic impact: The model's objective is to capture NVIDIA's patterns, especially if macroeconomic factors have limited predictive power for the stock.

Introduction:

This project aims to address several fundamental questions related to stock market analysis:
“How accurately can an LSTM model predict NVIDIA’s stock price using historical price data and technical indicators?”
“Does adding sentiment analysis as a feature improve the accuracy of NVIDIA’s stock price prediction?”
“Which technical indicators (e.g., moving average, volatility indicators) are most influential in predicting NVIDIA’s stock trends?”
“How does the model's predictive performance vary across different time periods, such as high vs. low volatility markets?”
“What is the impact of tuning hyperparameters on the LSTM model’s performance in stock prediction accuracy?”

Data Explotation:

Getting the Data
The stock data is fetched from Yahoo Finance using the pandas_datareader and yfinance libraries. The dataset includes the adjusted closing prices and trading volumes.




