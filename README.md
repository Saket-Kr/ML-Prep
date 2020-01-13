# ML-Prep


https://towardsdatascience.com/how-do-we-train-neural-networks-edd985562b73

# Gradient Descent(GD)
Derivative of the sum is the sum of the derivatives. Therefore, in order to compute the derivatives of the loss, we need to go through each example of our dataset. It would be very inefficient to do it every iteration of the Gradient Descent, because each iteration of the algorithm only improves our loss by some small step.

# Mini-batch Gradient
We approximate the derivative on some small mini-batch of the dataset and use that derivative to update the weights. Mini-batch isn’t guaranteed to take steps in optimal direction. In fact, it usually won’t. 

# Stochastic Gradient Descent(SGD)
Extreme version of mini-batch gradient descent with batch size equals to 1. 

# Fix/change the learning rates
https://techburst.io/improving-the-way-we-work-with-learning-rate-5e99554f163b

# An overview of gradient descent optimization algorithms
https://ruder.io/optimizing-gradient-descent/

# RMSprop
- Adaptation of rprop algorithm for mini-batch learning.
- Similar to Adagrad - it radically diminishes learning rates.
https://towardsdatascience.com/understanding-rmsprop-faster-neural-network-learning-62e116fcf29a

# Boosting algorithms - They play a crucial role in dealing with bias variance trade-off. The selection of sample is made more intelligently. We subsequently give more and more weight to hard to classify observations.
https://www.analyticsvidhya.com/blog/2015/09/complete-guide-boosting-methods/

# Bagging algorithms - Only controls for high variance in a model. It is an approach where you take random samples of data, build learning algorithms and take simple means to find bagging probabilities.

Machine Learning mostly have to deal with two Trade-offs,
1) Bias-Variance Trade-offs
2) Precision-Recall Trade-offs

Bias - Leads to a high error on training and test data.
Low Bias -- Predicted data points are close to the target. Also, the model suggests less assumptions about the form of the target function.
High-Bias -- Predicted data points are far from the target. Also, the model suggests more assumptions about the form of the target function.
Low-bias ML algos -- Decision Trees, k-Nearest Neighbors and Support Vector Machines.
High-bias ML algos -- Linear Regression, Linear Discriminant Analysis and Logistic Regression.

Read about Random Forrest - https://towardsdatascience.com/understanding-random-forest-58381e0602d2

Variance - Performs well on training data but has high error rates on test data.
Low Variance: Data points are close to each as a result close to function. Also, the model Suggests small changes to the estimate of the target function with changes to the training 
High Variance: Data points are spread and as a result far from the function. Suggests large changes to the estimate of the target function with changes to the training 
Examples of low-variance machine learning algorithms: Linear Regression, Linear Discriminant Analysis and Logistic 
Examples of high-variance machine learning algorithms: Decision Trees, k-Nearest Neighbors and Support Vector Machines.

# Parametric or linear machine learning algorithms often have a high bias but a low variance.
# Non-parametric or non-linear machine learning algorithms often have low bias but high variance.

Read about PCA - https://towardsdatascience.com/understanding-pca-fae3e243731d
Read about Neural Networks/Backpropagation - https://towardsdatascience.com/understanding-neural-networks-19020b758230
Read about Binomial Distribution - https://towardsdatascience.com/fun-with-the-binomial-distribution-96a5ecabf65b
