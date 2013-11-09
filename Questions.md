Why is least squares used when the decision tree is used to predict probability?
Is there ever an advantage to trying Gini or Entropy with decision trees, rather than Chi-square?

Least Squares compared with Maximum Likelihood: "Recall that in MLE we seek the parameter values that
are most likely to have produced the data. In LSE, on the other hand, we seek the parameter values that
provide the most accurate description of the data, measured in terms of how closely the model ﬁts the
data under the square-loss function."

In *Logistic Regression Using SAS*, it explains that ordinary least squares (OLS), weighted least squares (WLS) and maximum likelihood (ML) are all ways to estimate parameters for a logistic model *when the data is grouped in a contingency table*.  Weighted Least Squares corrects for heteroscedasticity.
When data consists of individual observations, maximum likelihood should be used.  
OLS requires heteroscedasticity, which is obviously violated since errors are either 0 or 1.
Also, you can't do OLS with logit because ln(p_i / (1 - p_i) ) is undefined when p_i is 0 or 1 so you can't minimize (ln(p_i_predicted / (1 - p_i_predicted) - ln(p_i_actual / (1 - p_i_actual)) )^2 because the ln(p_i_actual / (1 - p_i_actual)) terms will always be undefined


|Prediction Type  | Statistic                               | Comments  |
|-----------------|-----------------------------------------|-----------|
|Decisions        | Accuracy or Missclassfication           |           |
|Rankings         | Concordance                             |           |
|Estimates        | Average Squared Error or Maximum Likelihood |       |
