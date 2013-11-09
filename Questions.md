Why is least squares used when the decision tree is used to predict probability?
Is there ever an advantage to trying Gini or Entropy with decision trees, rather than Chi-square?

Least Squares compared with Maximum Likelihood: "Recall that in MLE we seek the parameter values that
are most likely to have produced the data. In LSE, on the other hand, we seek the parameter values that
provide the most accurate description of the data, measured in terms of how closely the model ﬁts the
data under the square-loss function."

Based on what I read in *Logistic Regression Using SAS*, it seems that ordinary least squares (OLS), weighted least squares (WLS) and maximum likelihood (ML) are all ways to estimate parameters for a logistic model.  Weighted Least Squares corrects for heteroscedasticity.

|Prediction Type  | Statistic                               | Comments  |
|-----------------|-----------------------------------------|-----------|
|Decisions        | Accuracy or Missclassfication           |           |
|Rankings         | Concordance                             |           |
|Estimates        | Average Squared Error or Maximum Likelihood |       |
