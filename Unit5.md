# Unit 5 -  Inference for categorical variables

#Sampling variable

We will sample (point estimate) population and deliver a $$\hat p$ of parameter of interest, whihc will be $\hat p \pm z^*SE_{\hat p}$

## CLT for Proportions
 
For sampling variable we can simplify problem by using binormal distribution.
$\hat p \sim N( mean = p, SE = \sqrt(\frac{p(1-p)}{n})))$
$Z = \frac{\hat p - p}{SE}$


Conditions that need to be meet:

* * independence: in and between groups
	*  <10% of population
* sample skew
	* at least 10 successes and 10 failures
	* $n \hat p \geq 10$ and $ n(1 - \hat p) \geq 10$

###Additional notes

* The confidence level is about percentage of samples that yield intervals capturing the population parameter, not about predicting where future samples will fall. 
* If the CLT doesn't apply and the sample proportion is low (close to 0) the sampling distribution will likely be right skewed, if the sample proportion is high (close to 1) the sampling distribution will likely be left skewed.

##Reducing the confidence intervals

To reduce the confidence intervals we can use same approach as before and increase number of samples.
if we dont know probability, best approach is to be conservative and assume 50-50%

##Hypothesis test (proportions)

* We are testing against the population proportion (p).
* To calculate SE for sample or diff between two samples we will use exactly the same approach as last week.
* In hypothesis testing for one categorical variable, generate simulated samples based on the null hypothesis, and then calculate the number of samples that are at least as extreme as the observed data.


##Working with two categorical variables

* we will assume one to be explanatory (grouping) variable and other response variable.
* point estimate will be difference between two proportions
* $SE = z^* qrt{\frac{\hat p_1 (1- \hat p_1)}{n_1}+\frac{\hat p_2 (1- \hat p_2)}{n_2}}$
	* We always want population parameters (not sample statistics) in the hypotheses (both for conditions and standard error)
	* For confidence interval we use observed $\hat p$
* if we don't have known proportion we will use pool proportion $\hat p_ppol = \frac{\text{total success}}{\text{total n}}$
	* Our parameter of interest is p, affecting SE calculations (this does not happen with numerival variables where $\mu$ does not affect SE)

##Working with small samples

What if we got small sample other words when we don't meet success failure conditions ?
	* we will need to set up simulation to get our distribution
		* we base it on logic that p-value is P(observed or more extreme outcome | H0 is true)
		* we will repeat simulation a lot of times to do so

###Comparing two small sample proportions

* we create hypothesis on the difference
* we know that independence and success/failure requirements wont be meet
* we will simulate the difference now
* we will do test on the simulation

##Summary

* Use simulation methods when sample size conditions aren't met for inference for categorical variables.
	* t-distribution is only appropriate to use for means. When sample size isn't sufficiently large, and the parameter of interest is a proportion or a difference between two proportions, we need to use simulation.
* In hypothesis testing
	* for one categorical variable, generate simulated samples based on the null hypothesis, and then calculate the number of samples that are at least as extreme as the observed data.
	* for two categorical variables, use a randomization test.


#Chi-square GOF test

* Goodness of Fit test - how well observed data fits the expected distribution
	* we are comparing cdistribution of one categorical variable to a hypothesed distribution
* conditions of chi-square
	* samples must be independent
		* random
		* <10% of population
		* each case is counted only once
	* each scenario (cell) must have at least 5 expected cases
	* we will compare collected data against expected count in each group (cell)
* chi-square has only one parameter (df)
	* $\hat{\chi}^2= \sum_{k=1}^{n} \frac{(O_k - E_k)^2}{E_k}$ is based on difference between observed - expected in each group (cell)
	* p-value ofr a chi-square test is defined as tail area above the calculated test statistic


#Chi-square independence test 

We are evaluating relationship between two categorical variables.

**Test of independence** is based on $\hat{\chi}^2= \sum_{k=1}^{n} \frac{(O_k - E_k)^2}{E_k} with degrees of freedom calculated from $df = (R-1)(C-1)$ dependant on number of rows and columns
* conditions are the same as GOF
* expected count in two way table $= \frac{\text{row total} * \text{column total}{\text{table total}}
* we are evaluating relationship between two categorical variable



#Notes about the project

* https://class.coursera.org/statistics-004/forum/list?forum_id=10013
* If you want to turn off the exploratory analysis plot in the output of the inference function (you might want to do this in your projects to avoid repetitive graphs), you can simply add the argument eda_plot = FALSE to the function. Similarly, if you want to turn off the p-value plot, add inf_plot = FALSE. The defaults for both of these arguments are set to TRUE.
