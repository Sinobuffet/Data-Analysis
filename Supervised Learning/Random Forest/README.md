# Random forest
![image](https://user-images.githubusercontent.com/97000341/167240100-e08912b1-5688-4c0e-9882-bc218ddae172.png)

Random forest belongs to the Bagging (short for Bootstrap AGgregation) method in ensemble learning

Before explaining random forests, we need to mention decision trees. Decision tree is a very simple algorithm, which is highly explanatory and conforms to the intuitive thinking of human beings. This is a supervised learning algorithm based on if-then-else rules.

> ## Decision tree
> <img src="https://user-images.githubusercontent.com/97000341/167240156-e4dbbea9-76bd-4729-a2b6-93f2b1620d8e.png" width="500" ></img>
> 
> The decision tree algorithm adopts a tree structure and uses layer-by-layer reasoning to achieve the final classification. A decision tree consists of the following elements：
> * Root node: contains the complete set of samples
> * Internal Node: Corresponding Feature Attribute Test
> * Leaf nodes: represent the outcome of a decision
> 
> When predicting, a certain attribute value is used for judgment at the internal node of the tree, and which branch node to enter is determined according to the judgment result, until it reaches the leaf node, and the classification result is obtained.
> 
> Decision tree is the simplest machine learning algorithm. It is easy to implement, highly interpretable, fully in line with human intuitive thinking, and has a wide range of applications.

Random forest is composed of many decision trees, and there is no relationship between different decision trees.

When we carry out the classification task, new input samples enter, and each decision tree in the forest will be judged and classified separately. Each decision tree will get its own classification result, which one of the classification results of the decision tree is classified. At most, then the random forest will treat this result as the final result.

<img src="https://user-images.githubusercontent.com/97000341/167240261-8d4a0fd1-2afd-451b-924c-ee8afd61533a.png" width="500" ></img>


4 steps to construct a random forest
---
1. For a sample with a sample size of N, there are N times of replacement, one sample at a time, and finally N samples are formed. This selected N samples are used to train a decision tree as the samples at the root node of the decision tree.
2. When each sample has M attributes, when each node of the decision tree needs to be split, m attributes are randomly selected from these M attributes, satisfying the condition m << M. Then a certain strategy (say information gain) is used from these m attributes to select 1 attribute as the splitting attribute of this node.
3. In the process of decision tree formation, each node must be split according to step 2 (it is easy to understand that if the next attribute selected by the node is the attribute used when its parent node was split, the node has reached the leaf node, there is no need to continue to split). until it can no longer be divided. Note that no pruning is performed during the entire decision tree formation process.
4. Follow steps 1 to 3 to build a large number of decision trees, which constitutes a random forest.

Dataset
---
[California Housing Prices](https://www.kaggle.com/datasets/camnugent/california-housing-prices)

***Please note: I am using the kaggle data set here instead of the data set that comes with Sklearn (INDE 577 Lecture 8.2 used this one). They have different numbers of features***

Median house prices for California districts derived from the 1990 census.

This data takes the block as the smallest unit, and the corresponding information includes: population, median income, median house price, etc.

* longitude: A measure of how far west a house is; a higher value is farther west
* latitude: A measure of how far north a house is; a higher value is farther north
* housing_median_age: Median age of a house within a block; a lower number is a newer building
* total_rooms: Total number of rooms within a block
* total_bedrooms: Total number of bedrooms within a block
* population: Total number of people residing within a block
* households: Total number of households, a group of people residing within a home unit, for a block
* median_income: Median income for households within a block of houses (measured in tens of thousands of US Dollars)
* ocean_proximity: Location of the house w.r.t ocean/sea
* median_house_value: Median house value for households within a block (measured in US Dollars)


