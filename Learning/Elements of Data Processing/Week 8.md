---
date created: Wednesday, April 27th 2022, 3:17:07 pm
date modified: Friday, May 6th 2022, 11:57:41 am
---

# Week 8

## Supervised Vs Unsupervised

- supervised
    - classification
    - regression
- unsupervised
    - clustering
    - association

### Experimental Design (supervised)

- evaluation methods
- performance metrics
- feature selection

## Evaluation Methods

### The Generalisation Challenge

When a model learns too much from training data, it has

- low bias error
    - predicts well on training data
- high variance error
    - predictions change widely with different training data

### Training - Validation - Test

split the training data set to training set and validation set, and measure the performance of the model

### K-Fold Cross Validation

1. partition training data randomly into k blocks
2. Select the best hyper-parameters or model
    - repeat k times:
        - k - 1 blocks for training
        - 1 block for evaluation
    - average the k scores

### Bootstrap Validation

- sample: randomly drawn from the original dataset with replacement
- OOB: remaining unselected data are used for validation

## Performance Metrics

### Classification Metrics

$$Accuracy = \frac{\#TP + \#TN}{n}$$

- misleading in imbalanced data sets

$$Recall = \frac{\#TP}{\#TP + \#FN}$$

- use recall when you do not want FN (false negative) (detect as many malicious programs as possible)

$$Precision = \frac{\#TP}{\#TP + \#FP}$$

- use precision when you do not want FP (false positive) (avoiding putting innocent person in prison)

$$F1 = 2 \times \frac{Precision \times Recall}{Precision + Recall}$$

Subset Accuracy: $$\frac{\sum^k_{i = 1} \#TP_i}{n}$$

Average Accuracy: $$\frac{\sum^k_{i = 1} \frac{\#TP_i + \#TN_i}{n}}{k}$$

### Regression Metrics

- Mean Square Error: $$MSE = \frac 1 N \sum^N_{i = 1} (Y_i - \hat{Y_i})^2 = \frac{SSE}{N}$$
    - lower is better
- Root Mean Square Error: $$RMSE = \sqrt{MSE}$$
    - most used measure
    - lower is better
- Mean Absolute Error: $$MAE = \frac 1 N \sum^N_{i = 1} |Y_i - \hat{Y_i}|$$
    - lower is better

> MSE and RMSE are more sensitive to outliers, while MAE are more robust.

## Feature Selection

evaluate the goodness of each feature

what makes a good feature:

- well correlated with the class
- not independent of class

### Mutual Information

higher mutual information ([[Elements of Data Processing/Week 6#Mutual Information]]) represent a higher correlation

### Chi-square $\chi^2$ - Null Hypothesis

$H_0$: a feature $a_1$ is independent of the class $c$.

draw 2 contingency table, one for observed value and the other for expected value.

$$\chi^2(a_1, c) = \sum_i \sum_j \frac{(O_{i, j} - E_{i, j})^2}{E_{i, j}}$$

If the calculated $\chi^2$ value is greater than the critical value (looked up from table), then we reject the $H_0$ hypothesis.

> extremely sensitive to sample size
