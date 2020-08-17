# Time_Series

## Time Series Analysis

### Data Analysis
We examined the Canadian dollar-Yen (cad-Jpy) exchange rates for the period 1992 - 2020 to determine whether there is any predictable behaviour.

The data shows a long-term weakening of the yen over the period, as seen in the below plot

![Price plot](Images/price_plot.PNG)

Using the HP filter we  extracted the noise and the trend. Then, plotted the price vs trend for the perios 2015 to present. 

![Price plot](Images/price_vs_trend.PNG)

There was a lot of short term fluctuations around the trend. Mainly, with the price falling below the trend line, indicating that the yen was undervalued during those periods.

### Forecasting Returns

We used both an ARMA and an ARIMA model  to forecast returns, with the following results:

ARMA 5-day Returns forecast

![ARMA 5 day returns forecast](Images/ARMA_5day_forecast.PNG)

The  ARMA used an order of (2,1). Except for the AR lag 2, the p-values were below 0.05  This model was a good fit.

ARIMA 5-day Futures Price Forecast
![ARIMA 5 day Forecast](Images/ARIMA_5day_forecast.PNG)

For ARIMA, we used order (5,1,1)
The model is forcasting a decline in the value of the yen. However, based on the p-values all greater than 0.05, the model is not a good fit.

### Volatility
The GARCH model was used to forecast volatility using an order (2,1)
![Volatility](Images/GARCH_volatility.PNG)

Based on the graph above, the forecast for CAD/JPY volatility is that it is expected to rise over the next 5 days.

## Regression Analysis

A  Linear Regression model was created and used to make predictions of future returns

Below is the results. From the test data, it seems the model is not reliable, as there is a big variance between the predicted returns and the actual returns. 

Here is a sample of the first 5 records:

 ![Actual vs Predicted Returns](Images/Actual_vs_Predicted_Returns.PNG)

 Visualization of first 20 predictions vs the true values:


 ![First 20 Predictions](Images/First_20_predictions.PNG)

The Root  Mean Squared Error (RMSE) were as follows:
Out of sample:0.6445805
In-sample: 0.8419946 

This means that the model performs better on the test data than the training data.