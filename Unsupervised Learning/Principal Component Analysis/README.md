Principal Component Analysis
---
![image](https://user-images.githubusercontent.com/97000341/167279648-6f7b046c-9c78-419b-ab1c-10af8fc9f777.png)


PCA, as can be seen from the name, is a method of picking key points of analysis. The principal component analysis method is to make the new variable, the principal component, become a linear combination of the original variable through appropriate mathematical transformation, and select a few principal components that have a larger proportion in the total amount of variation information to analyze things. The greater the proportion of the principal component in the amount of variation information, the greater its role in the comprehensive evaluation.

* Principle: Since there is a certain correlation among the many variables involved in the evaluation, there must be dominant factors. According to this, through the research on the relationship between the original variable and the internal structure of the correlation matrix, several comprehensive indexes that affect a certain element of the target variable are found out, so that the comprehensive index is a linear fit of the original variable.

Process and steps
---
1. **Standardization**

Normalize the range of input dataset variables so that each of them can be analyzed roughly proportionally. Simply put, it is to convert data with large differences into comparable data. For example, convert a variable of 0-100 to a variable of 0-1. This step can generally be done by subtracting the mean and dividing by the standard deviation of each variable's value.

<img width="196" alt="1651978447(1)" src="https://user-images.githubusercontent.com/97000341/167279713-1a29f800-293a-4748-a828-be482619aa51.png">

Standardized indicator variable formula:

<img width="123" alt="1651978433(1)" src="https://user-images.githubusercontent.com/97000341/167279707-024160f4-a22b-45ca-b1cb-bf5102e18ceb.png">

2. **Covariance matrix calculation**

See how the variables of the input dataset vary relative to the mean. See if there is any relationship between them.

3. **Calculate the eigenvectors and eigenvalues of the covariance matrix to identify the principal components**

Both eigenvectors and eigenvalues are linear algebra concepts that need to be calculated from the covariance matrix in order to determine the principal components of the data.

4. **eigenvectors**

Choose to keep all components or discard those less important (low eigenvalues) and form a vector matrix with other components, which we call eigenvectors

5. **Replot the data along the principal component axis**

Use the eigenvectors of the covariance matrix to form new eigenvectors, relocating the data from the original axes to the principal component axes (hence the name principal component analysis). This can be done by multiplying the transpose of the original dataset by the transpose of the feature vector.

Dataset
---
I use PCA and logistic regression to predict whether an examiner has diabetes

[Diabetes Dataset](https://www.kaggle.com/datasets/mathchi/diabetes-data-set/metadata)

This dataset is originally from the N. Inst. of Diabetes & Diges. & Kidney Dis.

|Attribute |
|---|
|Pregnancies|
Glucose	
BloodPressure	
SkinThickness	
Insulin	
BMI	
DiabetesPedigreeFunction
Age

