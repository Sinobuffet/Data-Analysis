Ensemble Learning
---

Ensemble learning belongs to machine learning. It is a "training idea", not a specific method or algorithm.

<img src="https://user-images.githubusercontent.com/97000341/167276152-d4b2bc04-3707-4fe4-b803-7031507e3299.png" width="500" ></img>

Ensemble learning will select some simple basic models for assembly.
There are two main ways to assemble these basic models:

### Bagging (short for bootstrap aggregating, also known as "bagging")
* The idea of bagging is that all basic models are treated the same, and each basic model has only one vote in hand. Then use democratic voting to get the final result.
* In most cases, the variance of the results obtained by bagging is smaller.
#### Specific process:

> 1. The training set is extracted from the original sample set. Each round draws n training samples from the original sample set using Bootstraping (in the training set, some samples may be extracted multiple times, and some samples may not be drawn at once). A total of k rounds of extraction are performed to obtain k training sets. (k > training sets are independent of each other)
> 2. Each time a training set is used to get a model, k training sets get a total of k models. (Note: There is no specific classification algorithm or regression method > here, we can use different classification or regression methods according to specific problems, such as decision trees, perceptrons, etc.)
> 3. For the classification problem: the k models obtained in the previous step are classified by voting method; for the regression problem, the mean of the above model > is calculated as the final result. (All models are of equal importance)
### Boosting
* The core idea of Boosting is to pick the elite.
* The most essential difference between Boosting and bagging is that he does not treat the basic model consistently. Instead, he tries to select the "elite" through constant testing and screening, and then gives the elite more voting rights. The poorly performing basic model gives Less voting rights, then combined with everyone's vote to get the final result.
* most of the time,The result bias  obtained by boosting is smaller.
#### Specific process:

> 1. The basic model is linearly combined by the addition model.
> 2. Each round of training improves the weight of the base model with a small error rate and reduces the weight of the model with a high error rate.
> 3. Change the weight or probability distribution of the training data in each round, and reduce the weight of the sample by the weak classifier in the previous round, > and reduce the weight of the previous round of the paired sample to make the classifier It has a good effect on misclassified data.

Adaboost algorithm
----

This project will mainly study the usage of Adaboost

![image](https://user-images.githubusercontent.com/97000341/167276421-45f9f598-8e4b-485b-b7da-4d24a2c06eec.png)


* AdaBoost is the first truly successful boosting algorithm developed for binary classification. This is the best starting point for understanding power. Modern boosting methods build on AdaBoost, most notably Stochastic Gradient Boosting Machines.

* AdaBoost is used for short decision trees. After the first tree is created, the performance of the tree on each training instance is used to weight the attention of * each training instance for the next tree created. Hard-to-predict training data is given more weight, while easy-to-predict instances are given less weight. Models are created sequentially, one after the other, and each model updates weights on the training instance that affect the learning performed by the next tree in the sequence. After all trees are built, predictions are made on new data and the performance of each tree is weighted according to the accuracy of the training data.

* Because the algorithm is so focused on correcting errors, clean data with outliers must be removed.
