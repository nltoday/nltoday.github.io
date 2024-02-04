---
layout: post
title: "Understanding Out-Of-Bag Errors and Bootstrapping in Random Forest Models"
date: 2023-12-29 16:50:21 +0000
categories: "Movies"
excerpt_image: https://editor.analyticsvidhya.com/uploads/79380OOB_Error_Example.png
image: https://editor.analyticsvidhya.com/uploads/79380OOB_Error_Example.png
---

Random forest models utilize two important concepts for improving accuracy and maintaining diversity among decision trees - out-of-bag errors and bootstrapping. Let's take a deeper look at what they are and how they help random forests work better.
### Leveraging Out-Of-Bag Samples  
Out-of-bag errors refer to the error estimates obtained from evaluating decision trees on data that was [not included](https://store.fi.io.vn/xmas-matching-outfits-for-holiday-chinchilla-christmas-tree-1) in their training set. This is a clever way random forests have of **internal validation** without requiring a separate test set. When building each tree, about one-third of the samples are left out and not used in the training process. These out-of-bag samples are then pushed down the tree to obtain a prediction. Comparing the actual values to the predictions on these out-of-bag samples gives an unbiased estimate of the generalization error of that particular tree.

![](https://www.baeldung.com/wp-content/uploads/sites/4/2021/08/out-of-bag-1024x497.png)
### Aggregating Diverse Learners
On their own, individual decision trees are prone to **overfitting the training data**. By averaging the predictions of many of these base learners, random forests aim to reduce variability and improve accuracy. However, if all trees made predictions based on the **same training samples**, there would be little diversity and the benefits of ensemble methods would be diminished. 
### The Need for Data Perturbation  
This is where **bootstrapping enters the picture**. When building each tree, a random sample with replacement is drawn from the original data. About one-third of samples on average will be left out and used as out-of-bag data for that tree. The rest are used to grow the tree but will be sampled multiple times. This simple sampling procedure introduces variation that encourages diverse learners.
### Better Generalization with Random Subspace Method
Diversity is further boosted through another technique called the **random subspace method**. At each node of every tree, instead of considering all features, only a random subset is used for finding the optimal split. This prevents all trees from being influenced by the same features. Together, bootstrapping and the random subspace method help random forests become more robust learners.
### Leveraging Correlations Among Predictions  
The true power of random forests lies in averaging predictions from many such de-correlated decision trees. **Averaging reduces variance** while retaining the same bias as a single tree. Furthermore, the out-of-bag estimates obtained from left-out samples provide an unbiased evaluation of a forest's true generalization ability during training.
### Identifying Important Predictors
Since each tree is grown independently on perturbed and partial datasets, variable or **feature importance** can also be directly calculated as the average increase in error without that predictor across all trees. This provides valuable feature selection without additional computation.
### Scope for Hyperparameter Tuning
While random forests work reasonably well with their **default hyperparameters**, there is still room for improvement through tuning. Parameters like the number of variables considered at each split or the number of trees can significantly impact performance on certain datasets. With careful validation, random forests offer a powerful and interpretable machine learning approach.
### Summary 
In this article, we discussed how random forests leverage two key techniques - **bootstrapping and out-of-bag validation** - to build a committee of **decorrelated** and **diverse** decision trees. By averaging predictions from these base learners, they achieve significantly better generalization than a single tree model. The random subspace method and internal validation using out-of-bag samples complete the design of this highly effective machine learning algorithm.
![Understanding Out-Of-Bag Errors and Bootstrapping in Random Forest Models](https://editor.analyticsvidhya.com/uploads/79380OOB_Error_Example.png)