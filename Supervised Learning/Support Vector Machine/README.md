Support Vector Machine
---

Support Vector Machines are probably one of the most popular and talked about machine learning algorithms.

![image](https://user-images.githubusercontent.com/97000341/167271258-13e5bdaf-6957-4e86-990e-f911786eca6f.png)

A hyperplane is a line that divides the input variable space. In SVM, the hyperplane is chosen to optimally separate points in the input variable space from their class (class 0 or class 1). In 2D, you can think of it as a line and assume that all our input points can be completely separated by this line. The SVM learning algorithm finds the coefficients that cause the hyperplane to best separate the classes.

<img src="https://user-images.githubusercontent.com/97000341/167271039-61e79bd2-fa81-4b19-ab2d-0779a1b2f582.png" width = "50%" />

The distance between the hyperplane and the nearest data point is called the margin. The best or best hyperplane that can separate the two classes is the line with the largest margin. Only these points are related to the construction of the definition hyperplane and classifier. These points are called support vectors. They support or define hyperplanes. In fact, the optimization algorithm is used to find the value of the coefficient that maximizes the margin.

SVM is probably one of the most powerful out-of-the-box classifiers, and it's worth trying to use your data set.

 

The basic concepts of support vector machines can be explained by a simple example. Let's imagine two categories: red and blue. Our data has two characteristics: x and y. We want a classifier that gives a pair of (x,y) coordinates and the output is limited to red or blue. We will list the marked training data in the following figure:

<img src="https://user-images.githubusercontent.com/97000341/167271089-ceeaf5b9-c8e4-419c-a675-ce0861a83fb3.png" width = "50%" />

The support vector opportunity accepts these data points and outputs a hyperplane (in a two-dimensional graph, a line) to separate the two categories. This line is the decision boundary: split red and blue.


<img src="https://user-images.githubusercontent.com/97000341/167271106-619cc9ac-3e6c-4332-bd06-3dba6e7b5d34.png" width = "50%" />

Dataset
---




