k−NearestNeighbor
---
<img src="https://user-images.githubusercontent.com/97000341/167274169-4d61aa28-73f2-475f-abea-2f8aba48e669.png" width="500" ></img>


The KNN algorithm is very simple and very efficient. The model representation of KNN is the entire training dataset.


Predictions for new data points are made by searching the entire training set of the K most similar instances (neighbors) and summarizing the output variables of those K instances. For regression problems this might be the mean output variable, for classification problems this might be the mode (or most common) class value.

The trick is how to determine the similarity between data instances. If your attributes have the same scale (e.g. in inches), the easiest technique is to use Euclidean distance, which you can compute directly from the difference between each input variable.

KNN can require a lot of memory or space to store all the data, but only compute (or learn) when predictions are needed, in time. You can also update and curate your training instances over time to keep predictions accurate.

Algorithmic mechanism
---
Given a data set of test samples, find the k closest training samples in the training set based on some distance metric, and then make predictions based on the information of these k neighbors.

<img src="https://user-images.githubusercontent.com/97000341/167274234-6b9f2849-00d0-4b1a-a95c-e2406ea1c7b8.png" width="500" ></img>

> When k = 3 , it belongs to category B
> 
> When k = 6 , it belongs to category A

It can be seen from the results that k is an important parameter, and different values of k will lead to different classification results.

#### The specific process is as follows:

* Calculate the distance between the points in the dataset of known classes and the test sample points;
* Arrange the calculated results in ascending order;
* According to the selected k, take out the first k sample points in the sorted list;
* The category to which the first k sample points belong, and the frequency of occurrence of the category;
* The category with the highest frequency is used as the prediction result of the current test sample point.


Dataset
---
[Fruits with colors dataset](https://www.kaggle.com/datasets/mjamilmoughal/fruits-with-colors-dataset?resource=download)

The dataset uses the four column features of mass, height, width, and color_score for fruit classification


The fruits dataset was created by Dr. Iain Murray from University of Edinburgh. He bought a few dozen oranges, lemons and apples of different varieties, and recorded their measurements in a table. And then the professors at University of Michigan formatted the fruits data slightly
