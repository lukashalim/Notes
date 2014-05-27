### Backpropagation for Neural Networks
- For each training example, use the gradient (the vector of partial derivatives) of the cost function to determine how to change the weights so as to minimize the cost. 
- When the partial derivative is large, that indicates that changing the weight of the neuron can substantially improve performance - in other words, the neuron has a lot of error. On the other hand, if the partial derivative is small, changing the weight will not improve performance, indicating the neuron does not have much error.
- Steps in Algorithm:
 - Pick network architecture (number of hidden layers, number of hidden units)
 - Train Neural Network
  - Randomly Initialize Weights
  - Implement forward propogation to compute output vector for training examples
  - Implement code to compute the cost function
  - Implement backprop to compute the partial derivatives of the cost function
  - Use gradient checking to compare the partial derivatives computed using backprop to the numerical estimate of the cost function
  - Use gradient descent or advanced optimization method with backprop to try to minimize the cost as a function of the parameters
- Gradient Checking is a less computationally efficient way of computing deriviatives than backprop, but it is used to confirm that backprop has been properly implemented.


No local minimum for least squared error on OLS, aside from the global minimum
"Batch" gradient descent - "batch" means you use entire training set

### Improving performance of machine learning algorithm
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

### Recommender Systems
- Big interest in Silicon Valley, less academic interest
- Collaborative Filtering
 - for cases when obeservations do not have features. Ex - movies without information about how romantic of funny they are
 - minimize features and coefficients simultaneously

### Large Scale Machine Learning
- Beause batch Gradient descent doesn't scale well, we consider some variants with better performance for large data sets
 - Batch Gradient Descent: use all examples in each iteration
 - stochastic gradient descent: use 1 examples in each iteration
 - mini-batch gradiet descent: use b examples in each iteration
- Online Learning Algorithms
- use each new example to update learning algorithm
- example: decide what search results to show based on what users are clicking on
- useful if things you are predicting may be slowly changing over time
- Map Reduce and Data Parallelism
 - Batch Gradient Descent
  - performs algorithm on 1/n of the data on each of n machines
  - combined sum is equivalent to standard batch gradient descent
 - Many learning algorithms can be expressed as computings sums of functions over the training set

### Photo OCR case study
- OCR = Optical Character Recognition
- Difficult to recognize characters in photos
- Steps:
 - text detection: identifying regions with text
 - character segmentation: identifying separations between characters
 - character classification: identifying characters
- 
