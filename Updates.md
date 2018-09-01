# 9/1/18
-Variables are now transformed component-wise to standard normal distributions rather than standardized to mean 0 variance 1. This limits (but does not completely eliminate) the infuence of outliers so that the null distribution can be more accurately estimated. Outliers often exist with, for example, multiplicative noise.

# 6/10/17
-Added a permutation option to estimate the null (approx="perm"). May be better for smaller sample sizes, although the permutation doesn't change the fact that non-linear regression is difficult with few samples.

-Separated RCIT and RCoT into two different functions. 

-Added KCIT from (Zhang et al., 2011).

# 5/8/17
Added an additional method for estimating the null distribution called "chi2" which normalizes the empirical partial cross-covariance matrix so that it asymptotically follows a Gaussian with diagonal covariance (after root-n multiplication). The resultant statistic therefore asymptotically obeys a central chi-squared distribution with 25 degrees of freedom rather than a weighted sum of chi-squares. I find that the p-values are slightly less accurate than the default method in general. On the other hand, the new method outputs a normalized statistic, so the statistics are comparable without the same random seed. This method may be useful in algorithms like HITON-PC which initially sort variables according to the test statistic.
