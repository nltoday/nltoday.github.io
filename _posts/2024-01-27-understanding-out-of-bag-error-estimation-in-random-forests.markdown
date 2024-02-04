---
layout: post
title: "Understanding Out-of-Bag Error Estimation in Random Forests"
date: 2024-01-27 11:49:54 +0000
categories: "Healthy food"
excerpt_image: https://editor.analyticsvidhya.com/uploads/79380OOB_Error_Example.png
image: https://editor.analyticsvidhya.com/uploads/79380OOB_Error_Example.png
---

## The Importance of Model Validation
It is crucial for any machine learning model to be properly validated before being deployed. If a model overfits the training data and does not generalize well to new samples, then it will not perform accurately when making real-world predictions. One common technique is to split the available data into a training set and a held-out validation or test set. However, when the dataset is small, this can further reduce the amount of data available for training. Out-of-bag error estimation provides a way to validate random forest models internally without requiring a separate validation set.
### Random Forests and Bagging
Random forests work by building an ensemble of decision trees trained on randomly sampled subsets of the data, called bagging. Each tree is constructed using a different bootstrap sample, which involves randomly sampling [with replacement](https://store.fi.io.vn/chihuahuas-rockin-the-dog-mom-aunt-life-chihuahua-womens-funny-chihuahua-dog) from the original dataset to create a training set of the same size. This means some samples will be used multiple times while others may be omitted. The excluded samples not contained in each bootstrap training set are known as the **out-of-bag samples**.

![](https://iq.opengenus.org/content/images/2022/09/out-of-bag-error-plot.png)
### Validating with Out-of-Bag Samples 
After a tree is fully grown on its bootstrap training set, the out-of-bag samples that were not used in its construction are put down the tree to obtain predictions. By aggregating the predictions of trees where each sample was out-of-bag, we can estimate its prediction error without using a dedicated validation set. The out-of-bag error is calculated as the proportion of times the true class does not match the predicted class for each sample, averaged over all samples.
## How Out-of-Bag Error Works in Practice
### Using OOB Samples Internally 
Through bagging and bootstrapping, on average about one-third of the original samples will be left out of each bootstrap training set and can be used as an internal validation set. This means that for a forest of say 500 trees, each sample effectively gets "voted" on by around 167 trees where it was out-of-bag.
### Unbiased Performance Estimate
Research has shown the out-of-bag error estimate to be nearly as accurate as validation against a completely separate holdout test set, while avoiding the need to explicitly split or reserve a portion of the originally available data just for validation purposes. This makes out-of-bag error an important tool for unbiased evaluation of random forest models.
### Tracking Error over Training
The out-of-bag samples can also be used to monitor for overfitting during the training process. By calculating the out-of-bag error after construction of each additional tree and tracking if it decreases or levels off, we can determine when adding more trees stops yielding performance improvements. This helps determine the optimal number of trees needed.
## Understanding Variable Importance
Out-of-bag samples also enable evaluation of the importance of each feature or variable in the model. Feature importance indicates how useful or relevant each predictor variable is to the task.
### Measuring Importance from Prediction Changes
To measure the importance of a variable, its values are randomly permuted in the out-of-bag data and that data is passed down the trees to obtain new predictions. The difference in prediction accuracy before and after permutation directly relates to how important that variable was for prediction. More important variables will cause a larger decrease in accuracy when perturbed.
### Ranking Features by Importance Score
This process is repeated for each variable to obtain an importance score. Variables can then be ranked based on these scores, with higher numbers indicating more predictive power. This gives insights into which features the model relies on most. It also allows reducing future models to just the most useful subset of variables in order to improve performance and simplify the solution.
## Additional Applications of Out-of-Bag Data
### Finding Optimal Model Parameters
Beyond validation and feature selection, out-of-bag samples have additional benefits. Tunable hyperparameters like the number of randomly selected features considered at each split can be optimized using a grid search monitored by out-of-bag error. This helps ensure the model is configured to generalize well.
### Detecting Outliers or Anomalies  
Samples significantly different from the training distribution may be detectable as outliers with abnormally low proximity to their nearest neighbors in the same class. An **outlier score** computed from out-of-bag proximities could flag potential anomalies in new data needing further inspection.
### Clustering and Data Visualization
The proximities calculated while building random forests can also be used for unsupervised tasks like clustering and dimensionality reduction through metric multidimensional scaling. This sheds light on inherent patterns and groupings present in the data in a way that informs supervised modeling as well.
## Conclusion
By leveraging samples left out of each tree's training during bagging, random forests enable powerful forms of internal validation and interrogation of models without requiring a holdout test set. Out-of-bag error estimation, feature importance, hyperparameter tuning, outlier detection and dimensional reduction are all facilitated through intelligently re-purposing data not consumed by the trees. This makes random forests highly self-sufficient and practical even when available data is scarce.
![Understanding Out-of-Bag Error Estimation in Random Forests](https://editor.analyticsvidhya.com/uploads/79380OOB_Error_Example.png)