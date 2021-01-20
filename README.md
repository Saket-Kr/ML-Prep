The choice of machine learning algorithm solely depends on the type of data. If you are given a data set which exhibits linearity, then linear regression would be the best algorithm to use. If you given to work on images, audios, then neural network would help you to build a robust model. If the data comprises of non linear interactions, then a boosting or bagging algorithm should be the choice. If the business requirement is to build a model which can be deployed, then we’ll use regression or a decision tree model (easy to interpret and explain) instead of black box algorithms like SVM, GBM etc. In short, there is no one master algorithm for all situations. We must be scrupulous enough to understand which algorithm to use.

### NNs
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

### Machine Learning mostly have to deal with two Trade-offs
1) Bias-Variance Trade-offs
2) Precision-Recall Trade-offs

### Bias
Leads to a high error on training and test data. Low Bias, when predicted data points are close to the target. Also, the model suggests less assumptions about the form of the target function. High-Bias, when predicted data points are far from the target. Also, the model suggests more assumptions about the form of the target function.

**Low-bias ML algos**: 
   - Decision Trees 
   - k-Nearest Neighbors
   - Support Vector Machines
   
**High-bias ML algos**:
   - Linear Regression 
   - Linear Discriminant Analysis
   - Logistic Regression.

### Variance 
Performs well on training data but has high error rates on test data. Low Variance: Data points are close to each as a result close to function. Also, the model Suggests small changes to the estimate of the target function with changes to the training. High Variance: Data points are spread and as a result far from the function. Suggests large changes to the estimate of the target function with changes to the training.

**Low-variance algos**: 
   - Linear Regression 
   - Linear Discriminant Analysis
   - Logistic
   
 **High-variance algos**: 
   - Decision Trees 
   - k-Nearest Neighbors 
   - Support Vector Machines.

*Parametric or linear machine learning algorithms often have a high bias but a low variance. Non-parametric or non-linear machine learning algorithms often have low bias but high variance.*

Read about PCA - https://towardsdatascience.com/understanding-pca-fae3e243731d
Read about Neural Networks/Backpropagation - https://towardsdatascience.com/understanding-neural-networks-19020b758230
Read about Binomial Distribution - https://towardsdatascience.com/fun-with-the-binomial-distribution-96a5ecabf65b
Read about Random Forrest - https://towardsdatascience.com/understanding-random-forest-58381e0602d2

---------------------------------------------------------------------------------------------------------------------------------

### sum of squares of regression 
https://365datascience.com/sum-squares/ 

### R-squared
https://365datascience.com/r-squared/
Zero means our regression line explains none of the variability of the data, 1 would mean our model explains the entire variability of the data. It measures the goodness of fit of our model. The more factors we include in our regression, the higher the R-squared.

### Adjusted R-squared
Always smaller than the R-squared, as it penalizes excessive use of variables. *We will consider adjusted R² as opposed to R² to evaluate model fit because R² increases irrespective of improvement in prediction accuracy as we add more variables. But, adjusted R² would only increase if an additional variable improves the accuracy of model, otherwise stays same*.

**naive bayes - bayes theorem formula - application**  
https://monkeylearn.com/blog/practical-explanation-naive-bayes-classifier/#feature-engineering  
box plot - inter-quartile range -   
bias/variance - corrections.  
variance - regularisation - L1, L2 - advantage/cons  
Ridge regression, lasso regression - https://towardsdatascience.com/regularization-in-machine-learning-76441ddcf99a  
lstm - forward/back propagation  
bi-directional rnn  
gru -   
precision/recall - roc/area under - when to choose roc/recall/precision - not do precision when data is imbalanced, recall when less data available class's is req.(credit fraud/cancer detection) / F1 score  

**ROC** - bank defaulters - check the threshold value for classifiation, with different threshold values, accuracy changes
ROC is a plot of signal (True Positive Rate) against noise (False Positive Rate). The model performance is determined by looking at the area under the ROC curve (or AUC). The best possible AUC is 1 while the worst is 0.5 (the 45 degrees random line). Any value less than 0.5 means we can simply do the exact opposite of what the model recommends to get the value back above 0.5.

gradient descent - formmulas 
when to use different algos.
Random forrest when features are too much
**Naive bayes** - features are indep, overfitting avoid
P(A|B) = P(A ∩ B) / P(B)
Similarly, P(B|A) = P(A ∩ B) / P(A)
It follows that P(A ∩ B) = P(A|B) * P(B) = P(B|A) * P(A)
Thus, P(A|B) = P(B|A)*P(A) / P(B)
P(A) is called **Prior probability** and P(B) is called **Evidence**.
The underlying assumption of these classifiers is that all the features used for classification are independent of each other, and hence the name **Naive**.

Linear - features are 1000s, overfitting avoid, less computation needed
isolation forest 
- https://github.com/h2oai/h2o-tutorials/blob/master/tutorials/isolation-forest/isolation-forest.ipynb
- https://github.com/h2oai/h2o-tutorials/blob/master/tutorials/isolation-forest/interpreting_isolation-forest.ipynb
Feature engg - https://towardsdatascience.com/feature-engineering-for-machine-learning-3a5e293a5114 
PCA -  
Ensemble boosting  
Random sampling with replacement  

A parsimonious model is a model that accomplishes a desired level of explanation or prediction with as few predictor variables as possible.

**idf(w)** = log(total number of documents/number of documents containing word w)  
**tf(w)** = doc.count(w)/total words in doc  
**Tf-idf(w)** = tf(w)*idf(w)  

**Confusion Matrix**: (TP + TN) / (TP + TN + FP + FN)  
**Recall** = TP / (TP + FN)  
Recall can be defined as the ratio of the total number of correctly classified positive examples divide to the total number of positive examples. High Recall indicates the class is correctly recognized (small number of FN). Recall is the ability of a classifier to find all positive instances. For each class, it is defined as the ratio of true positives to the sum of true positives and false negatives.  
**Precision** = TP / (TP + FP)
Precision is the ability of a classifier not to label an instance positive that is actually negative. For each class, it is defined as the ratio of true positives to the sum of true and false positives.  
To get the value of precision we divide the total number of correctly classified positive examples by the total number of predicted positive examples. High Precision indicates an example labeled as positive is indeed positive (small number of FP).
 
*High recall, low precision*:This means that most of the positive examples are correctly recognized (low FN) but there are a lot of false positives.

*Low recall, high precision*:This shows that we miss a lot of positive examples (high FN) but those we predict as positive are indeed positive (low FP)
 
**F-measure**: (2 * Recall * Precision) / (Recall + Precision)
Since we have two measures (Precision and Recall) it helps to have a measurement that represents both of them. We calculate an F-measure which uses Harmonic Mean in place of Arithmetic Mean as it punishes the extreme values more. The F-Measure will always be nearer to the smaller value of Precision or Recall. The F1 score is a weighted harmonic mean of precision and recall such that the best score is 1.0 and the worst is 0.0.  

**Principal Component Analysis (PCA)** - In the real world, we deal with multi-dimensional data. Thus, data visualization and computation become more challenging with the increase in dimensions. In such a scenario, we might have to reduce the dimensions to analyze and visualize the data easily. We do this by:  
- Removing irrelevant dimensions
- Keeping only the most relevant dimensions  
This is where we use Principal Component Analysis (PCA).  
Finding a fresh collection of uncorrelated dimensions (orthogonal) and ranking them on the basis of variance are the goals of Principal Component Analysis.  
The Mechanism of PCA:  
- Compute the covariance matrix for data objects
- Compute the Eigen vectors and the Eigen values in a descending order
- To get the new dimensions, select the initial N Eigen vectors
- Finally, change the initial n-dimensional data objects into N-dimensions  


Datasets: https://medium.com/towards-artificial-intelligence/best-datasets-for-machine-learning-data-science-computer-vision-nlp-ai-c9541058cf4f
