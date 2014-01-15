Multicollinearity
- explanatory variables are highly correlated
- inflates standard errors on the regression coefficients
- can potentially switch expected sign of a regression coefficient

Dealing with Multicollinearity
- Exclude Redundant variables
- redefine variables
- *Penalized Regression Techniques* also called *Biased Regression Techniques*
- center the independent variables in polynomial regression models

Biased Regression Techniques
- intentionally biases the estimation of the regression techniques
- tend to have more precision than OLS esitimates in the presence of multicollinearity
- MSE(Beta_hat) = [Bias(Beta_hat)^2] + Var(Beta_hat)
- ![img](/screenshots/bias.PNG)
- in OLS, bias for your Betas are set to zero
- in Biased regression, bias can vary, allowing us to get smaller values of MSE

Many Different Techniques for Biased Regression
- Principal Components Regression (PCR)
 - use some of the principal components
 - for interpetability, you can work out regression equation with the original variables.
 ![img](/screenshots/PCR_Interpretation.PNG)
 - Disadvantages - may not always work.
 - Can be distorted by outliers which alter the variance-covariance matrix
- Ridge Regression

Independence (or lack thereof)
- extension of independence is that explanatory variables are independent of the errors - called exogenous variables E(eplilon|X) = 0.
- explanatory variables are correlated with the errors - endogenous 
- Instrumental Variable

Endogeneity
- your x values are correlated with your errors
- correct by using 'instrumental' variables to model your endogenous variables. however, we don't want to model them *perfectly*, because that will preserve endogenity

Dealing with Heteroscedasticity
- compromises the standard errors of the parameter estimates
- Var(AX) = A * Var(X) * A^T
