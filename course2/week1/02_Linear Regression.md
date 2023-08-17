## Learning Goals
- Linear Regression
- Modeling Best Practice
- Measuring Errors

## Linear Regression

![](img/6.png)

**Calculate the Residuals**

$y_\beta({x_{obs}^{(i)}}) - y_{obs}^{(i)}$

**Minimizing the Error Function**

$J(\beta_0, \beta_1) = \frac{1}{2m}\sum_{i=1}^m ((\beta_0 + \beta_1 x_{obs}^{(i)}) - y_{obs}^{(i)})^2 $

**Modeling Best Practice**

### Linear Regression: The Syntax
```
# Import the class containing the regression model
from sklearn.linear_model import LinearRegression

# Create an instance of the class
LR = LinearRegression()

# Fit the instance on the data
LR = LR.fit(X_train, y_train)

# Predict the expected value
y_pred = LR.predict(X_test)

```