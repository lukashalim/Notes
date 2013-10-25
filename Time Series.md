Time Series
=========


## AR(1) Model: 
![AR1](https://lh4.googleusercontent.com/CDOXRs0dlMJ66SXYFH8aXZN1Eo4hzMedwS9J2G5eHYihELI9aWL7iNyCaV_z1F7Wzg=w1254-h460)  
When |phi| < 1, the observations fluctuate around the mean and the time series is stationary.  When phi = 1, the model is called a Random Walk:  ![Random Walk](https://lh5.googleusercontent.com/gYfedblTWPtF6Ix0sIU-lC_BNGytgQE9wK8ekMUw4NRz5MTj5jdjfzRnVVb6XpGSUA=s190)

####Expanding AR(1):
![AR1](https://lh3.googleusercontent.com/tzN0ewuYA8Jee00rTRourQ6p2PmbCp89MA5VjVyj9gk1Hj8fpjeoWKK_PMpFvj99aw=w1254-h512)

As k increases, the size of the first term will stedily decrease, assumping |phi| < 1.  This is why we see the ACF decline.  

ARMA(1,1) model: ![ARMA(1,1)](https://lh4.googleusercontent.com/sPlbmK3Lkx5khh0uzmprqNl-XNQw94ndfzJeHCC7XplpMRblwLd_sWn6R5clA5q5Ew=s190) where theta is the moving average paramter

Box Jenkins Method
- Transform series, by applying operations such as logorithms and differences, to make it stationary
- Analyze and choose tentative ARMA specification
- estimate the model
- diagnostic checking
- forecasting

Question: What exactly is meant by "Stochastic Process"?  Does this term describe all time series problems?  One author writes, "In general, a collection of random variables x_t indexed by t is referred to as a stochastic process."

A linear combination of values in a time series is referred to as a "filtered series"

Random walk with drift ![Drift](https://lh4.googleusercontent.com/m5n2JQzGVYQjPsk_n87rIOfVpwSflNqa5zsTr6zWSH3DvbfSmeVklTS7OLYmGpbaBg=s190) where delta is the drift and w_t is white noise

 spectral analysis - technique for detecting periodic signals
 
 smooth time series will have autocovariance functions that stay high even when the time periods are far apart, while "choppy" time series functions will tend to have near zero autocovariance functions for large separations.
 
![ACF](https://lh3.googleusercontent.com/T_ccurkWpTIKlOJk1hogyUxquXcKNYtfbpIyMBvvfJkIZto3ybMe5AW95q_MJ3zFNg=w1254-h512)

(the funny symbol is the covariance function)

Handling Trend 
- With Regression: To remove the trend, we subtract the values predicted by least squares from the observed values.
- With Differencing
 - Advantage that it doesn't require estimating the trend
 - Disadvantage is that it doesn't result in an estimate of the stationary process 
 - First difference eliminates a linear trend, the second difference can remove a quadratic trend

Why is ACF=0 for lag > 1 for MA(1) but not for AR(1)?
Why does a random walk model lack stationarity?
Why is the ACF of a random walk 1 for all lags?
