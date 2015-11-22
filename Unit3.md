Book to look at:
* https://www.openintro.org/stat/textbook.php
* http://insideairbnb.com/get-the-data.html

# Unit 3

More samples we have less variables we have from the samples


##Central limit theorem

The distribution of sample statistics is nearly normal, centred at the population mean, and with a standard deviation equal to the population standard deviation divided by square root of the sample size.

Conditions:

* the sampled observations must be independent with respect to the variable in question - sampling need to be independent
* if sampling without replacement, sample **n < 10% of population**
* if population distribution is skew the sample size need to be large (30+)

OTher:

* Central Limit Theorem does not apply to the sampling distribution of medians

##Confidence intervals

* $\hat x = z \frac{s}{\sqrt n}$ where s is the sample standard error.
* $SE= \frac{\sigma}{\sqrt{n}}$, standard error is calculated using samples from the same population
* If we choose large confidence level (CL) we stop being informative.
* If we increase sample size we will increase precision and accuracy.
* we can estimate sample size required for a desired margin of error (ME) using $n=(\frac{z*s}{ME})^2$.
	* The critical value for confidence level can be found using qnorm((1-ConfienceLevel)/2) so for ex qnorm((1-.98)/2)
* significance level is complement to confidence level if we use two tail test in other words $CL = 1 - \alpha$ then.
* in case of one sided hypothesis it is $CL = 1 - 2\alpha$
* if H0 is rejected, a confidence level that agrees with the result of the hypothesis should not include the null value.


##Statistical inference

* We start with a sceptical null hypothesis $H_0$ representing status quo
* we create alternative hypothesis, representing our research question
* we conduct hypothesis either using:
	* simulation
	* theoretical methods
		* using normal distribution
* check conditions for CLT
* calculate test statistics
* if we can't reject $H_0$ based on the data (p-value), we stay with it. If we can, we reject $H_0$ in favour of $H_A$
	* to do so we will use p-value


##Hypotheses testing

* the [p value](https://en.wikipedia.org/wiki/P-value) is defined as the probability, under the assumption of hypothesis H, of obtaining a result equal to or more extreme than what was actually observed. Other words P(observed or more extreme outcome | H0 true)
	* for normal distribution we can calculate it as:
		* p = 2* pnorm(-abs(Z)) for two tail
		* p = pnorm(-abs(Z)) for one tail
* we assume that point estimate is unbiased that is provide a good estimate of parameter for ex
	* sample mean
	* difference between sample means
	* sample proportion
	* difference between sample proportion
* we create confidence interval for nearly normal point estimates
* decision errors
	* type I error - rejecting H0 when its true
		* we tend to mineralise the rate of type I error
		* $P(type I | H_0 true) = \alpha$
	* type II error - fail to reject H0 when alternative is true
		* $P(type II | H_0 true) = \beta$
		* $\beta$ depends on effect size, difference between point estimate and null value
		* power of the test $1 - \beta$
* or goal is to keep both errors low
* real difference between the point estimate and null value are easier to detect with larger samples
	* with very large samples we will have statistical significance (large Z and small p-value) even if the difference is not practically significant


#Mid term exam feedback


* p-value = P (observed or more extreme outcome | H0 true), "the probability of obtaining a random sample of 40 college students where the average reaction distance is 9.51 cm or less, if in fact the true average reaction distance of all college students is 10 cm."
* he two box plots below display distributions of midterm scores for all students in two different sections of a public policy course. Assume that both classes have an even number of students, and that none of the students within each section had identical scores.
	* It's impossible to tell because while we know that a score of 55 is below the 25th percentile for both distributions, we can't tell from the box plots what the actual percentile for this observation is under the two distributions.
* The distribution of the sample always mimics the population distribution. It's the shape of the sampling distribution that changes based on the sample size, not the shape of the sample distribution.
* Spread of the sampling distribution is the standard error
* Higher the magnitude of the Z score the more unusual the observation.
* In a normal distribution 68% of the observations are within one standard deviation of the mean. Q1 and Q3 mark the boundaries of the middle 50%, therefore they're closer to the median (and hence the mean, since in a symmetric distribution these values will be approximately the same) than the cutoff values for 1 SD away from the mean.