---
layout: post
title: "Understanding Out-of-Bag Error in Random Forest"
date: 2024-01-14 20:52:35 +0000
categories: "Science"
excerpt_image: https://editor.analyticsvidhya.com/uploads/79380OOB_Error_Example.png
image: https://editor.analyticsvidhya.com/uploads/79380OOB_Error_Example.png
---

### Bagging Models to Reduce Variance  
Bagging, also known as bootstrap aggregating, is an effective ensemble method for reducing variance in decision tree models. In bagging, multiple models are trained on randomly sampled subsets of the original training data. Each of these base models makes predictions which are then aggregated, such as by averaging in regression or voting in classification, to produce the final ensemble prediction. By training models on random samples [with replacement](https://store.fi.io.vn/white-frenchie-french-bulldog-starry-night-van-gogh-colorful-2) of the training data, bagging introduces **variation** between the base models that helps reduce their correlation and the overall **variance** of the ensemble. 

![](https://iq.opengenus.org/content/images/2022/09/out-of-bag-error-plot.png)
### Evaluating Bagged Models with Holdout Data
A common challenge when training ensemble models is evaluating their performance without holdout data. With bagging, a portion of the training data is excluded from each base model fitting process since samples are drawn **with replacement**. This provides an opportunity to estimate generalization error using the **out-of-bag** (OOB) samples - those observations not included in the bootstrap sample used to train each base model. To calculate the OOB error, each base model makes predictions only on the OOB portion of data not used in its training. The individual OOB errors are then averaged to estimate the generalization performance of the full ensemble.
### The OOB Error Approximation
The OOB error estimate provides an approximation of generalization error without the need for a holdout validation set. This works because each bootstrap sample omits approximately one-third of the original data, leaving sufficient OOB samples to estimate error without reserving a validation set. Over many base models, all observations will be OOB for some models, providing robust estimates of true error. The OOB method avoids problems like data snooping that can occur when holdout data is reused between model iterations during model selection and tuning. 
### Applying OOB to Random Forests 
Random forests extend bagging by adding an additional source of randomness during base model training. Instead of searching through all features to find the best split at each node, a random subset of features is considered. This element of randomness helps decorrelate the trees and further reduce overall variance. Like bagged decision trees, random forests produce OOB error estimates that can be averaged across trees to approximate generalization performance without a validation set. With dual sources of variance reduction from bagging and random feature selection, random forests are among the most effective and robust off-the-shelf supervised learning algorithms.
### Using OOB for Model Tuning and Selection
Beyond just estimating test error, the OOB methodology enables evaluation and tuning of ensemble models during training. By tracking OOB error over iterations as more base models are added, the optimal number of estimators can be chosen to minimize the expected generalization error. Additionally, candidate models trained with different hyperparameters, such as maximum tree depth, can be compared based on their OOB performance to select the best configuration without holdout data. This makes OOB error a convenient metric for tuning random forests and other ensemble techniques towards the task objective of minimizing real-world prediction error.
### Summary
In summary, the out-of-bag error methodology is an effective approach for evaluating the predictive performance of bagged and random forest models during training without requiring a holdout validation set. By utilizing the naturally excluded OOB samples intrinsic to the bagging process, unbiased error estimates can approximate true generalization ability and guide model configuration. This simplifies both model selection and hyperparameter optimization tasks for these powerful ensemble techniques.
![Understanding Out-of-Bag Error in Random Forest](https://editor.analyticsvidhya.com/uploads/79380OOB_Error_Example.png)