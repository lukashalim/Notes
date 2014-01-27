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
- your x values are correlated with your errors. As a result, your betas are biased.
![img](/screenshots/endogenous.PNG)
- Endogeneity occurs in two cases
 - Omitted Variables
 - Measurement Error
  - bias is only introduced when your dependent variable (for example, x1) is related to the measurement error for y
  - measurement error in the dependent variable always introduces bias
- Testing for Endogeneity
 - Regress suspected independent variable on all other independent variables
  - this gives us the 'extra' information provided by our suspect variable which is not provided by the other variables
  - trying to isolate out the bad part of the suspect variable
 - Keep residuals
 - Regress dependent variable on all variables (except instrumental ones) and the residuals from the prevous step
 - Test coefficient on residual variable
- Solutions to Endogeneity
 - Two-Stage Least Squares
  - instrumental variable exogeneous (not related to the error term) and related to an (endogenous) predictor variable
  - correct by using 'instrumental' variables to model your endogenous variables. however, we don't want to model them *perfectly*, because that will preserve endogenity
  - afterwords, we 

Dealing with Heteroscedasticity
- compromises the standard errors of the parameter estimates. Dr. L showed some of the math behind this - normal error estimates assume constant variance in independent variable
- does not bias coefficient estimates
- Tests for heteroscadasticity 
 - White and Breush
 - White tests all dependent variables and tends to be too lenient, while Breush looks at particular varible(s)
- Resolving heteroscadasticity 
 - Calculate Robust Standard Errors 
 - Weighted Least Squares: Weight individual observations
  - like ordinary least squares, but we assign weights to each observations, and find the minimum of the weighted squared errors.
  - can be used for multiple purposes - in time series, we can weight more recent observations more than older observations. we can also use it to limit the influence of outliers, and we can use it to handle heteroscadasticity.
  - In order to use weighted least squares with heteroscadasticity, we downweight the observations with dependent values that have higher heteroscadasticity. ex - if high income people have higher heroscadasticity, high income observations are downweighted.
 - Feasible Generalized Least Squares
  - estimate a function for heteroscadasticity using some of the dependent variables
  - use this function to set the weights for weighted least squares
 - if you just wand valid t-tests, one approach is to transform the predictor variables

Robust Regression
- Anamolous Observation
 - outliers: large standardized residual; far from the fitted line in the y-direction
 - leverage points: falls far outside the mean in the x-space
 - influential point / influential observations: point which influences regression
- Distributional outliers
 - typically we assume our distributions are normal, but if they are thick tailed, then we should expect large proportion of data which is far from the mean
 - a thick tailed distribution has a higher probability of producing larger errors that those that would be expecte from a Normal distribution.
- a good Robust Regression technique should be *close* to as good as OLS when data is uncontaminated and *better* than OLS when data is contaminated
- Types of Robust Regression
 - M-estimation: handles outliers
  - Huber's M-estimation: instead of minimizing sum of squared errors, minimize some other function of the errors
 - Least Trimmed Squares: handles leverage points
 - MM-estimation: handles both outliers and leverage points

Least Trimmed Squares
- mimimize squared errors, but "trim"

Panel Data
- sort of a mix of time-series and cross-sectional
- looking at entities over time
- poold regression
- fixed-effects
 - assuming that the subjects we have represent the entire population available to study or represent the entire population of interest
- random effects
 - used when you are trying to generalize from random sample to a bigger population
