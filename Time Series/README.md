### Time Series
Decompose time series into components, trend, seasonal, residual.  
**P** = Periods to lag for eg: (if P= 3 then we will use the three previous periods of our time series in the autoregressive portion of the calculation) P helps adjust the line that is being fitted to forecast the series. Purely autoregressive models resemble a linear regression where the predictive variables are P number of previous periods.

**D** = In an ARIMA model we transform a time series into stationary one(series without trend or seasonality) using differencing. D refers to the **number of differencing transformations required by the time series to get stationary**. Stationary time series is when the mean and variance are constant over time. It is easier to predict when the series is stationary.

**Q** = This variable denotes the lag of the error component, where error component is a part of the time series not explained by trend or seasonality.  
Autocorrelation refers to how correlated a time series is with its past values whereas the ACF is the plot used to see the correlation between the points, up to and including the lag unit. In ACF, the correlation coefficient is in the x-axis whereas the number of lags is shown in the y-axis.  
The Autocorrelation function plot will let you know how the given time series is correlated with itself.  
Normally in an ARIMA model, we make use of **either the AR term or the MA term**. We use both of these terms only on rare occasions. We use the ACF plot to decide which one of these terms we would use for our time series.  
**Read more about Time-series** - https://towardsdatascience.com/time-series-forecasting-arima-models-7f221e9eee06



Statsmodels.tsa.seasonal.seasonal_decompose  
Time series needs to be stationary because it easy to forecast and is more reliable. Autoregressive forecasting models are essentially linear regression models. Linear regression works best if predicators, X vars, are not correlated against each other. Stationarizing series solves this problem. We can make nearly any time series stationary by:  
1) Differencing the series
2) Take log  
3) e nth root  
4) combination of above  
*Most common is Differencing which is subtracting next value by current value. If series isn't stationary yet, do second differencing.*

**White noise** - A white noise process is one with a mean zero, constant variation and no correlation between its values at different times.  
Stationary series.   

**Detrend a time series**:  
Subtract the line of best fit from the time series. The line of best fit may be obtained from a linear regression model with the time steps as the predictor. For more complex trends, you may want to use quadratic terms (x^2) in the model.  
Subtract the trend component obtained from time series decomposition we saw earlier.  

Subtract the mean  

Apply a filter like Baxter-King filter(statsmodels.tsa.filters.bkfilter) or the Hodrick-Prescott Filter   (statsmodels.tsa.filters.hpfilter) to remove the moving average trend lines or the cyclical components.   

Deseasonalize a time series:  
Take a moving average with length as the seasonal window. This will smoothen in series in the process.  
Seasonal difference the series (subtract the value of previous season from the current value)  
Divide the series by the seasonal index obtained from STL decomposition  
If dividing by the seasonal index does not work well, try taking a log of the series and then do the deseasonalizing. You can later restore to the original scale by taking an exponential.  

Treat missing values in a time series  
1) Backward Fill  
2) Linear Interpolation  
3) Quadratic interpolation  
4) Mean of nearest neighbors  
5) Mean of seasonal couterparts  

If you have explanatory variables use a prediction model like the random forest or k-Nearest Neighbors to predict it.  
If you have enough past observations, forecast the missing values.  
If you have enough future observations, backcast the missing values  
Forecast of counterparts from previous cycles.  


estimate the forecastability of a time series  

The more regular and repeatable patterns a time series has, the easier it is to forecast. The ‘Approximate Entropy’ can be used to quantify the regularity and unpredictability of fluctuations in a time series.  

The higher the approximate entropy, the more difficult it is to forecast it.  

Another better alternate is the ‘Sample Entropy’.  

Sample Entropy is similar to approximate entropy but is more consistent in estimating the complexity even for smaller time series. For example, a random time series with fewer data points can have a lower ‘approximate entropy’ than a more ‘regular’ time series, whereas, a longer random time series will have a higher ‘approximate entropy’.  

Why and How to **smoothen** a time series: 
**Smoothening** of a time series may be useful in:  
- Reducing the effect of noise in a signal get a fair approximation of the noise-filtered series.
- The smoothed version of series can be used as a feature to explain the original series itself.
- Visualize the underlying trend better   
So how to smoothen a series? Let’s discuss the following methods:
- Take a moving average
- Do a LOESS smoothing (Localized Regression)
- Do a LOWESS smoothing (Locally Weighted Regression)

https://www.machinelearningplus.com/time-series/arima-model-time-series-forecasting-python/

https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/
