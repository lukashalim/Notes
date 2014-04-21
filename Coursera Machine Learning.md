No local minimum for least squared error on OLS, aside from the global minimum
"Batch" gradient descent - "batch" means you use entire training set

Diagnostics for improving machine learning algorthym
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
