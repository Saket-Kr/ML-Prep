### ML-Prep


https://towardsdatascience.com/how-do-we-train-neural-networks-edd985562b73

### Gradient Descent(GD)
Derivative of the sum is the sum of the derivatives. Therefore, in order to compute the derivatives of the loss, we need to go through each example of our dataset. It would be very inefficient to do it every iteration of the Gradient Descent, because each iteration of the algorithm only improves our loss by some small step.

### Mini-batch Gradient
We approximate the derivative on some small mini-batch of the dataset and use that derivative to update the weights. Mini-batch isn’t guaranteed to take steps in optimal direction. In fact, it usually won’t. 

### Stochastic Gradient Descent(SGD)
Extreme version of mini-batch gradient descent with batch size equals to 1. 

### Fix/change the learning rates
https://techburst.io/improving-the-way-we-work-with-learning-rate-5e99554f163b

### An overview of gradient descent optimization algorithms
https://ruder.io/optimizing-gradient-descent/

### RMSprop
- Adaptation of rprop algorithm for mini-batch learning.
- Similar to Adagrad - it radically diminishes learning rates.
https://towardsdatascience.com/understanding-rmsprop-faster-neural-network-learning-62e116fcf29a

### Boosting algorithms
They play a crucial role in dealing with bias variance trade-off. The selection of sample is made more intelligently. We subsequently give more and more weight to hard to classify observations.
https://www.analyticsvidhya.com/blog/2015/09/complete-guide-boosting-methods/

### Bagging algorithms
Only controls for high variance in a model. It is an approach where you take random samples of data, build learning algorithms and take simple means to find bagging probabilities.

### Machine Learning mostly have to deal with two Trade-offs,
1) Bias-Variance Trade-offs
2) Precision-Recall Trade-offs

### Bias
Leads to a high error on training and test data. Low Bias, when predicted data points are close to the target. Also, the model suggests less assumptions about the form of the target function. High-Bias, when predicted data points are far from the target. Also, the model suggests more assumptions about the form of the target function.
Low-bias ML algos -- Decision Trees, k-Nearest Neighbors and Support Vector Machines.
High-bias ML algos -- Linear Regression, Linear Discriminant Analysis and Logistic Regression.

### Variance 
Performs well on training data but has high error rates on test data. Low Variance: Data points are close to each as a result close to function. Also, the model Suggests small changes to the estimate of the target function with changes to the training. High Variance: Data points are spread and as a result far from the function. Suggests large changes to the estimate of the target function with changes to the training 
Markup: * Examples of low-variance machine learning algorithms: 
          *Linear Regression 
          *Linear Discriminant Analysis
          *Logistic 
Markup : * Examples of high-variance machine learning algorithms: 
           * Decision Trees 
           * k-Nearest Neighbors 
           * Support Vector Machines.

Markup : *Parametric or linear machine learning algorithms often have a high bias but a low variance. Non-parametric or non-linear machine learning algorithms often have low bias but high variance.

Read about PCA - https://towardsdatascience.com/understanding-pca-fae3e243731d
Read about Neural Networks/Backpropagation - https://towardsdatascience.com/understanding-neural-networks-19020b758230
Read about Binomial Distribution - https://towardsdatascience.com/fun-with-the-binomial-distribution-96a5ecabf65b
Read about Random Forrest - https://towardsdatascience.com/understanding-random-forest-58381e0602d2

### Time Series
Decompose time series into components, trend, seasonal, residual.
Statsmodels.tsa.seasonal.seasonal_decompose
Time series needs to be stationary. We can make nearly any time series stationary by:
a) Differencing the series
b) Take log
c) e nth root
d) combination of above
Most common is Differencing which is subtracting next value by current value. If series isn't stationary yet, do second differencing.

Making a series stationary is important because it easy to forecast and is more reliable. Autoregressive forecasting models are essentially linear regression models.

Linear regression works best if predicators, X vars, are not correlated against each other. Stationarizing series solves this problem.

White noise and stationary series. 

Detrend a time series:
Subtract the line of best fit from the time series. The line of best fit may be obtained from a linear regression model with the time steps as the predictor. For more complex trends, you may want to use quadratic terms (x^2) in the model.
Subtract the trend component obtained from time series decomposition we saw earlier.

Subtract the mean

Apply a filter like Baxter-King filter(statsmodels.tsa.filters.bkfilter) or the Hodrick-Prescott Filter (statsmodels.tsa.filters.hpfilter) to remove the moving average trend lines or the cyclical components.

Deseasonalize a time series:
Take a moving average with length as the seasonal window. This will smoothen in series in the process.
Seasonal difference the series (subtract the value of previous season from the current value)
Divide the series by the seasonal index obtained from STL decomposition
If dividing by the seasonal index does not work well, try taking a log of the series and then do the deseasonalizing. You can later restore to the original scale by taking an exponential.

treat missing values in a time series
a) Backward Fill
b) Linear Interpolation
Quadratic interpolation
Mean of nearest neighbors
Mean of seasonal couterparts

If you have explanatory variables use a prediction model like the random forest or k-Nearest Neighbors to predict it.
If you have enough past observations, forecast the missing values.
If you have enough future observations, backcast the missing values
Forecast of counterparts from previous cycles.


estimate the forecastability of a time series

The more regular and repeatable patterns a time series has, the easier it is to forecast. The ‘Approximate Entropy’ can be used to quantify the regularity and unpredictability of fluctuations in a time series.

The higher the approximate entropy, the more difficult it is to forecast it.

Another better alternate is the ‘Sample Entropy’.

Sample Entropy is similar to approximate entropy but is more consistent in estimating the complexity even for smaller time series. For example, a random time series with fewer data points can have a lower ‘approximate entropy’ than a more ‘regular’ time series, whereas, a longer random time series will have a higher ‘approximate entropy’.

Why and How to smoothen a time series

Smoothening of a time series may be useful in:

Reducing the effect of noise in a signal get a fair approximation of the noise-filtered series.
The smoothed version of series can be used as a feature to explain the original series itself.
Visualize the underlying trend better
So how to smoothen a series? Let’s discuss the following methods:

Take a moving average
Do a LOESS smoothing (Localized Regression)
Do a LOWESS smoothing (Locally Weighted Regression)

https://www.machinelearningplus.com/time-series/arima-model-time-series-forecasting-python/

https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/

### Logistic/ Linear Regression (slope/intercept) 
The slope indicates the steepness of a line and the intercept indicates the location where it intersects an axis, say y-axis. For example, a company determines that job performance for employees in a production department can be predicted using the regression model y = 130 + 4.3x, where x is the hours of in-house training they receive (from 0 to 20) and y is their score on a job skills test. The value of the y-intercept (130) indicates the average job skill score for an employee with no training. The value of the slope (4.3) indicates that for each hour of training, the job skill score increases, on average, by 4.3 points.

### sum of squares of regression 
https://365datascience.com/sum-squares/ 

### R-squared
https://365datascience.com/r-squared/
Zero means our regression line explains none of the variability of the data, 1 would mean our model explains the entire variability of the data. It measures the goodness of fit of our model. The more factors we include in our regression, the higher the R-squared.

### Adjusted R-squared
Always smaller than the R-squared, as it penalizes excessive use of variables.

svm. - parameters (epsilon, cost, gamma)
random forst - entropy, information gain
naive bayes - bayes theorem formula - application 
box plot - inter-quartile range - 
bias/variance - corrections.
variance - regularisation - L1, L2 - advantage/cons - ridge regression, lasso regression
lstm - forward/back propagation
bi-directional rnn
gru - 
precision/recall - roc/area under - when to choose roc/recall/precision - not do precision when data is imbalanced, recall when less data available class's is req.(credit fraud/cancer detection) / F1 score
roc - bank defaulters - check the threshold value for classifiation, with different threshold values, accuracy changes
gradient descent - formmulas 
  when to use different algos.
Random forrest when features are too much
Naive bayes - features are indep, overfitting avoid
Linear - features are 1000s, overfitting avoid, less computation needed
Unsupervision - anomaly detection, k means, isolation forrest
Feature engg
PCA - 
Ensemble boosting 
Random sampling with replacement

A parsimonious model is a model that accomplishes a desired level of explanation or prediction with as few predictor variables as possible.
