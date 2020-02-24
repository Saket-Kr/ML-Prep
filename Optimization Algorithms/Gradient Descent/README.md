A type of optimization algorithm that checks the slope at each step and accordingly changes the coefficients of the features.  

**Classification**:  
*On the basis of data ingestion*  
- Full Batch Gradient Descent Algorithm
- Stochastic Gradient Descent Algorithm  

*On the basis of differentiation techniques*  
- First order Differentiation
- Second order Differentiation

**Challenges**  
*Data Challenges*  
- If the data is arranged in a way that it poses a non-convex optimization problem. It is very difficult to perform optimization using gradient descent. Gradient descent only works for problems which have a well defined convex optimization problem.
- Even when optimizing a convex optimization problem, there may be numerous minimal points. The lowest point is called global minimum, whereas rest of the points are called local minima. Our aim is to go to global minimum while avoiding local minima.
- There is also a saddle point problem. This is a point in the data where the gradient is zero but is not an optimal point. We don’t have a specific way to avoid this point and is still an active area of research.  
*Gradient Challenges*   
- If the execution is not done properly while using gradient descent, it may lead to problems like vanishing gradient or exploding gradient problems. These problems occur when the gradient is too small or too large. And because of this problem the algorithms do not converge.  
*Implementation Challenges*  
- Most of the neural network practitioners don’t generally pay attention to implementation, but it’s very important to look at the resource utilization by networks. For eg: When implementing gradient descent, it is very important to note how many resources you would require. If the memory is too small for your application, then the network would fail.
- Also, its important to keep track of things like floating point considerations and hardware / software prerequisites.
