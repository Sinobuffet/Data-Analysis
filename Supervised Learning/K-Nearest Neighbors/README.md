k−NearestNeighbor
--

The KNN algorithm is very simple and very efficient. The model representation of KNN is the entire training dataset.

![image](https://user-images.githubusercontent.com/97000341/167274169-4d61aa28-73f2-475f-abea-2f8aba48e669.png)


Predictions for new data points are made by searching the entire training set of the K most similar instances (neighbors) and summarizing the output variables of those K instances. For regression problems this might be the mean output variable, for classification problems this might be the mode (or most common) class value.

The trick is how to determine the similarity between data instances. If your attributes have the same scale (e.g. in inches), the easiest technique is to use Euclidean distance, which you can compute directly from the difference between each input variable.

KNN can require a lot of memory or space to store all the data, but only compute (or learn) when predictions are needed, in time. You can also update and curate your training instances over time to keep predictions accurate.
