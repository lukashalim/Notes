Power
- Probabiltiy that the null hypothesis is rejected, given that the null hypothesis is false
- effected by alpha, sample size, effect size, distribution

Observed Power
- assuming that the observed effects and variability are equal to the true parameters, the probability of rejecting the null hypothesis is computed
- advocates of observed power argue that there is evidence for the null hypothesis being true if the statistical significance was not achieved despite the computed power being high at the observed effect size

Power and Sample Size
- Power: 1-Beta. The chance that one detects a difference from the null hypothesis, if a difference as extreme as the alternative exists
- Power usually set to 80% or more, but you have to think about the consequences of a Type II error.
- For the same effect size, the higher the power the higher the sample size required
- Smaller alpha => lower power
- smaller standard deviation => higher power

- Prospetive vs. Retrospective Power Analysis
 - Prospective is *good*, while retrospective is *bad*
 
- Power for binomial distribution (for example, response to credit card offer)
 - distribution is not continuous, so PROC POWER always give an alpha that is below your specified alpha

Sawtooth Power Function
- Normally, the larger the sample, the greater the power
- However, with discrete data you cannot acheive the exact alpha desired, so a smaller than desired alpha is chosen. Since power is a function of alpha, this results in a decrease in power.

Test of Two Independent Proportions
- Pearson chi-squared (SAS default)
- Likelihood ratio test
- Fisher's exact test: use for cases with small expected cell frequencies (less than 5)
Effect sizes represented as
- proportion difference
- odds ratio
- relative risk
Sample Size Allocation
- common sample size per group (balanced design)
- sample size allocation weights for two groups
- two group sample size
