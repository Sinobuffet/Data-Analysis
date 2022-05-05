# Linear Regression

Linear Regression is a machine learning algorithm based on supervised learning. It performs a regression task. Regression models a target prediction value based on independent variables. It is mostly used for finding out the relationship between variables and forecasting. Different regression models differ based on – the kind of relationship between dependent and independent variables they are considering, and the number of independent variables getting used.

![image](https://user-images.githubusercontent.com/97000341/166848173-039def44-3fc3-4413-9c3e-ccfe4c9ada43.png)

Linear regression performs the task to predict a dependent variable value (y) based on a given independent variable (x). So, this regression technique finds out a linear relationship between x (input) and y(output). Hence, the name is Linear Regression.
In the figure above, X (input) is the work experience and Y (output) is the salary of a person. The regression line is the best fit line for our model.

**Hypothesis function for Linear Regression :**

![image](https://user-images.githubusercontent.com/97000341/166848197-2de311c8-e8ea-4e68-8877-f6bf0b68ef0f.png)

While training the model we are given :
* x: input training data (univariate – one input variable(parameter))
* : labels to data (supervised learning)

When training the model – it fits the best line to predict the value of y for a given value of x. The model gets the best regression fit line by finding the best θ1 and * θ2 values.
* θ1: intercept
* θ2: coefficient of x

Once we find the best θ1 and θ2 values, we get the best fit line. So when we are finally using our model for prediction, it will predict the value of y for the input value of x.

---
How to update θ1 and θ2 values to get the best fit line ?

Cost Function (J):
By achieving the best-fit regression line, the model aims to predict y value such that the error difference between predicted value and true value is minimum. So, it is very important to update the θ1 and θ2 values, to reach the best value that minimize the error between predicted y value (pred) and true y value (y).

![image](https://user-images.githubusercontent.com/97000341/166848397-4c8668ad-4968-4ffe-b623-7482639789f0.png)

![image](https://user-images.githubusercontent.com/97000341/166848403-4a501e17-76c9-42a6-a0b4-585df0ab14a9.png)

Cost function(J) of Linear Regression is the Root Mean Squared Error (RMSE) between predicted y value (pred) and true y value (y).
