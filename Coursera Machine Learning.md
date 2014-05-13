No local minimum for least squared error on OLS, aside from the global minimum
"Batch" gradient descent - "batch" means you use entire training set

### Improving performance of machine learning algorthym
- Mulitiple possible avenues to try
 - increasing/decreasing smoothing parameter
 - find more training examples
 - add/remove more features or add polynomial features
- Deciding what do try to improve model is a *Model Selection Problem*
 - Professor Ng recommends using training, (cross) validation, and test data sets, so that multiple models can be created using the training data, the model performing best on the (cross) validation can be selected, and then performance can be measured on the test set.
 
Bias and Variance
- Bias = Underfit
 - high training error, training and test error are similar
- Variance = Overfit
 - low training error, greater test error

Fixing High Variance
- Reduce number of features
- Increase regularization parameter
- Get more training examples

Fixing High Bias
- Increase number of features
- Decrease regularatization parameter

Far too often, people just try one method of improving model rather than systematically listing and then evaluating options.

Recommended Approach
- Create and implement learning algorithym and test on cross validation data
- plot curves to determine if more data or more features might help
- Error analysis: manually examine misclassified examples in the cross validation set to see if you can find systematic trend in types of examples algorithym is making errors on.
- Having a single value for model error, such as misclassficiation rate, is very helpful as you try to decide what options lead to the best learning algorithym performance

Choosing Error Metrics
- Misclassficiation rate can be misleading for skewed classes. If the event we are trying to predict is rare, we can just assume it never happens and get a great misclassification rate.
- Precision: True Positives / Predicted Positives
- Recall: True Positives / Actual Positives
- if you use a higher cuttoff for predicting the rare event, your precision improves but your recall gets worse
- if you use a lower cuttoff, precision decreases but recall increases

Sometimes More Data Does the Trick!
Important 2001 paper by Banko and Brill: http://acl.ldc.upenn.edu/P/P01/P01-1005.pdf?origin=publication_detail
"It's not who has the best algorthym that wins. It's who has the most data."
Useful test: Given the data, could a human expert make a confident prediction?

### Support Vector Machines
- Rather than creating additional features such as interactions, SVM use a kernal function to create features.
- Gaussian kernel is most common non-linear kernel. Measures distance.
- SVM with linear kernel is very similar to logistic regression.
- with large number of observations, Guassian kernel can get too slow
- Similar results to neural network, but SVM can be faster to train, and with frequently used kernels will certainly converge.

One-vs-All: Used for multilevel target for both logistic and SVM. Train a classifier, theta, for each factor level. On a new input, pick level with the maximum predicted probability

### Anamoly Detection
- Unsupervised approach to model probability of a given set of measurements.
- You can a simpler approach, which assumes no correlation between features, or an approach using a correlation matrix which allows for correlations. The latter requires more data and is computationally more expensive.
