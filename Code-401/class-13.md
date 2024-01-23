# Class 13

## Linear Regression

### Regression

Regression analysis is an important field of statistics and mathematics. It is a set of statistical processes for estimating the relationships of dependent and independent variables.

Regression is important to answer how some actions can influence other actions. 

### Linear Regression

Linear regression is a specific type of regression technique where you take the intersectionality of multiple variables and shove them into a line. To do this, it uses estimators to define an estimated function in order to calculate an estimated response.

Here are some conveniently placed key concepts of linear regression:

- Best Fit – the straight line in a plot that minimizes the deviation between related scattered data points.
- Coefficient – also known as a parameter, is the factor a variable is multiplied by. In linear regression, a - coefficient represents changes in a Response Variable (see below).
- Coefficient of Determination – the correlation coefficient denoted as 𝑅². Used to describe the precision or degree of fit in a regression. 
- Correlation – the relationship between two variables in terms of quantifiable strength and degree, often referred to as the ‘degree of correlation’.  Values range between -1.0 and 1.0. 
- Dependent Feature – a variable denoted as y in the slope equation y=ax+b. Also known as an Output, or a Response. 
- Estimated Regression Line – the straight line that best fits a set of scattered data points.
- Independent Feature – a variable denoted as x in the slope equation y=ax+b. Also known as an Input, or a predictor. 
- Intercept – the location where the Slope intercepts the Y-axis denoted b in the slope equation y=ax+b. 
- Least Squares – a method of estimating a Best Fit to data, by minimizing the sum of the squares of the differences between observed and estimated values.
- Mean – an average of a set of numbers, but in linear regression, Mean is modeled by a linear function.
- Ordinary Least Squares Regression (OLS) – more commonly known as Linear Regression. 
- Residual – vertical distance between a data point and the line of regression (see Residual in Figure 1 below).
- Regression – estimate of predictive change in a variable in relation to changes in other variables (see Predicted - Response in Figure 1 below).
- Regression Model – the ideal formula for approximating a regression.
- Response Variables – includes both the Predicted Response (the value predicted by the regression) and the Actual - Response, which is the actual value of the data point (see Figure 1 below).
- Slope – the steepness of a line of regression. Slope and Intercept can be used to define the linear relationship between two variables: y=ax+b.
- Simple Linear Regression – a linear regression that has a single independent variable.  
[source](https://www.activestate.com/resources/quick-reads/how-to-run-linear-regressions-in-python-scikit-learn/)

### SciKit-Learn

SciKit is a package that can be used in Python to work with regressions.

This is an example of how to create a linear regression model based on numpy array data:

```
# Import the packages and classes needed in this example:
import numpy as np
from sklearn.linear_model import LinearRegression
# Create a numpy array of data:
x = np.array([6, 16, 26, 36, 46, 56]).reshape((-1, 1))
y = np.array([4, 23, 10, 12, 22, 35])
# Create an instance of a linear regression model and fit it to the data with the fit() function:
model = LinearRegression().fit(x, y) 
# The following section will get results by interpreting the created instance: 
# Obtain the coefficient of determination by calling the model with the score() function, then print the coefficient:
r_sq = model.score(x, y)
print('coefficient of determination:', r_sq)
# Print the Intercept:
print('intercept:', model.intercept_)
# Print the Slope:
print('slope:', model.coef_) 
# Predict a Response and print it:
y_pred = model.predict(x)
print('Predicted response:', y_pred, sep='\n')
```

### Train/Test

Train test split is a model valdation process that allows you to simulate how your model would perform with new data.

In order to do so, you
1. Arrange the data:
    - Make sure your data is arranged into a format acceptable for train test split. In scikit-learn, this consists of separating your full data set into “Features” and “Target.”
2. Split the data:
    - Split the data set into two pieces — a training set and a testing set. This consists of random sampling without replacement about 75 percent of the rows (you can vary this) and putting them into your training set. The remaining 25 percent is put into your test set. Note that the colors in “Features” and “Target” indicate where their data will go (“X_train,” “X_test,” “y_train,” “y_test”) for a particular train test split.
3. Train the model:
    - Train the model on the training set. This is “X_train” and “y_train” in the image.
4. Test the model:
    - Test the model on the testing set (“X_test” and “y_test” in the image) and evaluate the performance.

The consequences of not using test train split would be a lacking performance on new data and an overly complex model that overfits on the data set.

## Things I want to know more about
