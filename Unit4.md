# Unit 4 -  Inference for numerical variables

## t-distribution

We use it when $\sigma$ is unknown (almost always). Due to shape confidence level for t- distribution will be wider. 

* to calculate critical t score we use R *abs(qt((1-.95)/2,df=21))*
* to calculate two tail p value we use * 2*pt(Z,df=df, lower.tail =F) *

##Interference on multiple variables

* For two variables standard error of difference will be: $\bar{x}_1-\bar{x}_2 \pm SE_{\bar{x}_1-\bar{x}_2} = \bar{x}_1-\bar{x}_2 \pm  \sqrt[]{\frac{s^2_1}{n_1}+\frac{s^2_2}{n_2}}$ where df will be min of any deg of freedom
* we would like both variables to be independent of each other
* interpretation: *those who eat with distractions consume 1.83 g and 48.17 g more snacks than those who eat without distractions, on average.*

What if it dependent?
	- they will be paired
	- we estimate different
	- we do hypothesis on difference
	- we estimate p-val = *pt(abs(Z),df=df, lower.tail = F)* 


## Power

Power of the test is the probability of correctly rejecting H0, and probability of doing so is $1 - \beta$. Our goal for any experiment is to keep $\alpha$ and $\beta$ low, but decreasing one increase the other one. Solution here is to increase the sample size.

How can we calculate what is the best sample size for the give power?

* we calculate SE for the difference from $s = \sqrt{\frac{s^2_1}{n_1}+\frac{s^2_2}{n_2}}$
* we calculate critical value for our significance level from  abs(qnorm((1-.95)/2))
* we calculate rejection region from RR = CriticalValue*s
* we define what effect we are trying to detect and estimate the power from $\frac{EffectSize-RR}{s}$
* how large sample size we need to calculate desired power?	
	* estimate needed power as percentile from qnorm(.8) (PV)
	* estimate a new SE from $SE = \frac{EffectSize}{PV+CriticialValue}$
	* use first equation for s to estimate n needed while given SE as s.

##ANOVA

side-by-side box plots are useful to compare numerical and categorical variables.
Analysis of variance (ANOVA) only answers whether there is evidence of difference in at least one pair of groups, it doesn’t tell us which groups are different.

Conditions:

* independence: in and between groups
	* each group has to be <10% of population
* approximate normality for each groups
* equal variance for each group

Which means are different? Most important problem here is type I error, as we increase it for the multiple tests. We tend to use Bonferroni correction for multiple comparisons (another one is Turnkey) by adjusting $\alpha^* = \frac{2 \alpha}{k(k-1)}$

##Bootstrapping

* The distribution is skewed, so the median is a better measure of the typical observation.

It is impossible to estimate a population parameter from only one sample. This is why we use bootstrapping. 

* Bootstrap distributions are constructed by sampling with replacement from the original sample, while sampling distributions are constructed by sampling with replacement from the population.
* Bootstrap distributions are centered at the population parameter, sampling distributions are centered at the sample statistic.

1. Take a bootstrap sample (a random sample with replacement of size equal to the original sample size) from the original sample.
2. Record the mean of this bootstrap sample.
3. Repeat steps (1) and (2) many times to build a bootstrap distribution.
4. Calculate the XX% interval using
	* the percentile method by estimating middle 95% of bootstrap distribution;
	* the standard error method - by calculating error and spread of bootstrap distribution ($t_*SE_{boot}$ with deg of freedom from original distribution), this is more precise.

Note that if bootstrap distribution is extremely skewed or sparse, the bootstrap interval might be unreliable. Its accuracy will be depending on the quality of the sample.

#links

https://www.codecademy.com/courses/learn-sql
