# Gradient Descent
![image](https://user-images.githubusercontent.com/97000341/166850328-ffb945c1-0661-4578-be76-b582c7117d39.png)


Gradient descent method 
---
Gradient descent method is used to find the minimum value of a function, and it is an iterative algorithm, which is often used in machine learning due to high computer efficiency. The gradient descent method often finds the minimum value of convex functions (such as various cost functions in machine learning), because the convex function has only one minimum value, and the minimum value obtained by using the gradient descent method is the minimum value. The corresponding gradient ascent method is used to find the maximum value of the function. The principle of the two methods is the same, but the sign is different in the calculation process.
> Mathematical definition of convex function: a real-valued function on a convex subset (interval) of a vector space, if at any two points on its domain, f(tx + (1-t)y) <= tf( x) + (1-t)f(y), then it is called a convex function on this interval.  
>
Not all functions have a minimum, we need to ensure that a convex function has a minimum. So in the objective function constructed by yourself, before applying any algorithm, make sure that it is a convex function.

Gradient
----
Gradient means that the directional derivative of a function at that point takes the maximum value along the direction. This concept is relatively abstract. Let’s compare it with going down the mountain. A person stands on a certain mountainside on the mountain and wants to go down the mountain at the fastest speed, so how to go down the mountain as quickly as possible? He just takes a small step at a time in the direction of the steepest and easiest downhill at the current position, and then continues to take a small step in the direction of the steepest position at the next position. Step by step like this, until we reach the point where we feel that we have reached the foot of the mountain. Then the steepest direction down the mountain is the negative direction of the gradient, and this method is the gradient descent method.

![image](https://user-images.githubusercontent.com/97000341/166850137-d737e97f-3121-483a-868b-b09307d9a8df.png)


How to find the gradient of a function? 
---
That is the derivative of this function at the current position. 
as function

![image](https://user-images.githubusercontent.com/97000341/166850072-2d99d71d-c38d-4fe5-9502-9e753b9732ac.png)

it's gradient is:

![image](https://user-images.githubusercontent.com/97000341/166850131-a28dc111-3147-4f03-ad1d-dc7d29bbcbc2.png)

How to use gradient descent algorithm? 
---
It is to first select an initial point, calculate the gradient of this point, and then update the independent variable in the direction of the gradient until the value of the function changes very little or reaches the maximum number of iterations. 

The value of k iterations is

![image](https://user-images.githubusercontent.com/97000341/166850222-c2359321-a56a-4e1f-97ec-f04e4e2b89b5.png)

The result of gradient descent method is

![image](https://user-images.githubusercontent.com/97000341/166850260-b669b26c-04ce-4bf3-9f7d-79505c942c37.png)

where alpha is called the step size or learning rate, and represents the size of the change in each iteration update. It stops until the function value changes very little or when the maximum number of iterations is reached, at which point the function is considered to have reached a minimum point.

# Dataset
---
[Auto MPG](https://archive.ics.uci.edu/ml/datasets/auto+mpg)

This dataset is a slightly modified version of the dataset provided in the StatLib library. In line with the use by Ross Quinlan (1993) in predicting the attribute "mpg", 8 of the original instances were removed because they had unknown values for the "mpg" attribute. The original dataset is available in the file "auto-mpg.data-original".

The data concerns city-cycle fuel consumption in miles per gallon, to be predicted in terms of 3 multivalued discrete and 5 continuous attributes.

