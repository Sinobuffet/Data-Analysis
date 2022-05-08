K-Means
---

k-means is a clustering algorithm whose workflow is as follows: randomly select k points as initial centroids (the centroid is the center of all points in a cluster), and then assign each point in the dataset to a cluster Specifically, find the nearest centroid for each point and assign it to the cluster corresponding to the centroid. After this step, the centroid of each cluster is updated to be the average of all points in that cluster. Repeat the above steps until the centroid does not change.

![image](https://user-images.githubusercontent.com/97000341/167278859-1f4c4a44-ff3b-4b72-a452-f9073d1d1d3c.png)

Algorithm steps:

1. (Randomly) select the initial centers of the K clusters;

2. For any sample point, find the distance to the K cluster centers, and classify the sample point into the cluster with the center with the smallest distance, and so on for n times;

3. During each iteration, the center point (centroid) of each cluster is updated by methods such as the mean value;

4. For K cluster centers, after using 2 and 3 steps of iterative update, if the position point changes very little (the threshold can be set), it is considered to have reached a stable state, and the iteration is over. Choose a different color callout.

### Advantage 
1) The principle is relatively simple, the implementation is also very easy, and the convergence speed is fast.
2) The clustering effect is better.
3) The interpretability of the algorithm is relatively strong.
4) The main parameter that needs to be adjusted is only the number of clusters k.

### Shortcoming 
1) The selection of K value is not easy to grasp
2) It is difficult to converge for non-convex data sets
3) If the data of each hidden category is unbalanced, for example, the amount of data of each hidden category is seriously unbalanced, or the variance of each hidden category is different, the clustering effect is not good.
4) The final result is related to the selection of the initial point, and it is easy to fall into the local optimum.
5) Sensitive to noise and outlier comparison.

Dataset
---

We explore k-means using the [wine](http://archive.ics.uci.edu/ml/datasets/Wine) dataset

These data are the results of a chemical analysis of wines grown in the same region in Italy but derived from three different cultivars. The analysis determined the quantities of 13 constituents found in each of the three types of wines.

|Attributes| 
|---|
|Alcohol
|Malic acid
Ash
Alcalinity of ash
Magnesium
Total phenols
Flavanoids
Nonflavanoid phenols
Proanthocyanins
Color intensity
Hue
OD280/OD315 of diluted wines
Proline
