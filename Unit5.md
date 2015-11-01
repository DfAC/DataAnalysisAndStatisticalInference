# Unit 5 -  Inference for categorical variables

#Sampling variable

We will sample (point estimate) population and deliver a $$\hat p$ of parameter of interest, whihc will be $\hat p \pm z^*SE_{\hat p}$

## CLT for Proportions -  
 
For sampling variable we can simplify problem by using binormal distribution.
$\hat p \sim N( mean = p, SE = \sqrt(\frac{p(1-p)}{n})))$
$Z = \frac{\hat p - p}{SE}$
Conditions:

* * independence: in and between groups
	*  <10% of population
* sample skew
	* at least 10 successes and 10 failures


The confidence level is about percentage of samples that yield intervals capturing the population parameter, not about predicting where future samples will fall. 

##Reducing the confidence intervals

To reduce the confidence intervals we can use same approach as before and increase number of samples.
if we dont know probability, best approach is to be conservative and assume 50-50%

##Hypothesis test

Same as last week.

##Working with two categorical variables

* we will assume one to be explanatory (grouping) variable and other response variable.
* point estimate will be difference between two proportions
* $SE = z^* qrt{\frac{\hat p_1 (1- \hat p_1)}{n_1}+\frac{\hat p_2 (1- \hat p_2)}{n_2}}$
* 