**Linear Regression**

- Among various regression methods available, Linear regression is one. Here we try to find a function that maps some features or variables to others sufficiently well.

- When implementing linear regression of some dependent variable 𝑦 on the set of independent variables 𝐱 = (𝑥₁, …, 𝑥ᵣ), where 𝑟 is the number of predictors, you assume a linear relationship between 𝑦 and 𝐱: 𝑦 = 𝛽₀ + 𝛽₁𝑥₁ + ⋯ + 𝛽ᵣ𝑥ᵣ + 𝜀. This equation is the regression equation. 𝛽₀, 𝛽₁, …, 𝛽ᵣ are the regression coefficients, and 𝜀 is the random error.

- Linear regression calculates the estimators of the regression coefficients or simply the predicted weights, denoted with 𝑏₀, 𝑏₁, …, 𝑏ᵣ. They define the estimated regression function 𝑓(𝐱) = 𝑏₀ + 𝑏₁𝑥₁ + ⋯ + 𝑏ᵣ𝑥ᵣ.

- The differences 𝑦ᵢ - 𝑓(𝐱ᵢ) for all observations 𝑖 = 1, …, 𝑛, are called the residuals.

- To get the best weights, you usually minimize the sum of squared residuals (SSR) for all observations 𝑖 = 1, …, 𝑛: SSR = Σᵢ(𝑦ᵢ - 𝑓(𝐱ᵢ))². This approach is called the method of ordinary least squares.

- The coefficient of determination, denoted as 𝑅², tells you which amount of variation in 𝑦 can be explained by the dependence on 𝐱 using the particular regression model. Larger 𝑅² indicates a better fit and means that the model can better explain the variation of the output with different inputs.

- The value 𝑅² = 1 corresponds to SSR = 0, that is to the perfect fit since the values of predicted and actual responses fit completely to each other.

- *Asymptote:* Straight line that continually approaches a given curve but does not meet it at any finite distance. Sigmoid function becomes asymptote to y=1 for positive values of x and becomes asymptote to y=0 for negative values of x.

Concept of **slope** and **intercept**:  
The estimated regression function has the equation 𝑓(𝑥) = 𝑏₀ + 𝑏₁𝑥.
  - *Intercept*: The value of 𝑏₀, is also called the intercept. It shows the point where the estimated regression line crosses the 𝑦 axis. It is the value of the estimated response 𝑓(𝑥) for 𝑥 = 0. For example, in the equation 𝑓(𝑥) *= 140 + 4.3*𝑥 The value of the y-intercept indicates the average job skill score for an employee with no training. The value of the slope (4.3) indicates that for each hour of training, the job skill score increases, on average, by 4.3 points.

  - *Slope*:  The value of 𝑏₁ determines the slope of the estimated regression line. It indicates the steepness of a line and the intercept indicates the location where it intersects an axis, say y-axis. For example, a company determines that job performance for employees in a production department can be predicted using the regression model y = 130 + 4.3x, where x is the hours of in-house training they receive (from 0 to 20) and y is their score on a job skills test.

***The polynomial regression** problem can be solved as a linear problem with the term 𝑥² regarded as an input variable.*
