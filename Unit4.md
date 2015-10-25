# Unit 4 -  Inference for numerical variables

## t-distribution

We use it when $\sigma$ is unknown (almost always). Due to shape confidence level for t- distribution will be wider. 

* to calculate critical t score we use R *abs(qt((1-.95)/2,df=21))*
* to calculate two tail stats we use * 2*pt(2.3,df=21, lower.tail =F) *
* For two variables standard error of difference will be: $\bar{x}_1-\bar{x}_2 \pm SE_{\bar{x}_1-\bar{x}_2} = \bar{x}_1-\bar{x}_2 \pm  \sqrt[]{\frac{s^2_1}{n_1}+\frac{s^2_2}{n_2}}$ where df will be min of any deg of freedomdddd
		* we would like both variables to be independent of each other
		* interpretation: *those who eat with distractions consume 1.83 g and 48.17 g more snacks than those who eat without distractions, on average.*
		* what if it dependent?
			* they will be paired
			* we estimate different
			* we do hypothesis on difference
			* we estimate p-val = *pt(abs(Z),df=df, lower.tail = F)* 


## Power

Power of the test is the probability of correctly rejecting H0, and probability of doing so is $1 - \beta$. Our goal for any experiment is to keep $\alpha$ and $\beta$ low, but decreasing one increase the other one. Solution here is to increase the sample size.

How can we calculate what is the best sample size for the give power?

* we calculate SE for the difference from \sqrt{\frac{s^2_1}{n_1}+\frac{s^2_2}{n_2}}$
* we calculate Z for our significance level from 


#links

https://www.codecademy.com/courses/learn-sql
