Book to look at:
* https://www.openintro.org/stat/textbook.php
* http://insideairbnb.com/get-the-data.html

# Unit 2

##Random process

$0\leq P(A) \leq1$

* frequentist interpretation - The probability of an outcome is the proportion of times the outcome would occur if we observed the random process an infinite number of times.
* bayesian interpretation - probability as a subjective degree of belief. We can use a prior estimations.
* law or large numbers  - when we collect a lot of observations we will converge towards the mean
* law of averages, gamblers fallacy is misunderstanding of the law or large numbers

##General addition rules

* disjoin events can't happen at the same time (mutually exclusive) P(A and B) = 0
	* P(A or B) = P(A) + P(B)
* non-disjoin events can happen at the same time $P(A and B) \neq 0$
 	* P(A or B) = P(A) + P(B) - P(A and B)

##Sample space
 
* Sample space - Collection of all possible outcome
* probability distribution - list all possible outcome with their probabilities, following those rules:
	* events listed must be disjoin
	* each probability 0-1
	* sum of probabilities == 1
* complementary events - two mutually exclusive events, whose probability adds to 1
* independence - two processes are independent if knowing outcome of one does not provide information about outcome of the other
	* dependence check P (A | B) = P(A)P(B)

#Conditional probability

* marginal, joint, conditional probability
	* use margins of the conditional table
	* for joint, it is intersect of circles, so intersect of specific row and column / Total of marginal distribution (all events)
	* conditional probabilities is same, intersect of specific row (B event) and column (A event) / marginal probability - total of row (only A event); other words $P(A|B) = \frac{P(A \cap B)}{P(B)}$
* Bayes' theorem and Bayesian Inference
	* posterior probability - probability of hypothesis, given the data we just observed 
		* P(hypothesis | data)
		* this is different to p-value - probability of observed or more extreme value being true,  given null hypothesis
	* in Bayesian approach we will evaluate claims iteratively as wel collect more data
	* good prior helps, but hurts, they matter less as we collect more data
* general product rule


#Normal distribution

* we assme |Z|>2 to be unusual
* normal distribution plots
	* data is on Y, theoretical quantilies on X. If fits to straight line data is normally distributed
		* right skew - point bend up and to the left
		* left skew - point bend down and to the right of the line
		* short tail - points follow S shape
		* long tail - point start below the line, bend to follow it  

#Binomial distribution

When an individual trial has only two possible outcomes, it is called a Bernoulli random variable. 
* The binomial distribution describes the probability of having exactly k successes in n independent Bernouilli trials with probability of success p. $\left( ^n _k \right) = \frac{ n! }{ k! \left( n-k \right)! }$ . For R its *choose* function. 
* Probability can be calcuated from $\left( ^n _k \right)p^k(1-p)^{(n-k)}$. For R its *dbinom* function. 
* $\mu = np$ and $\sigma = \sqrt{np(1-p)}$
* when no of observations increase Binomial Distribution will be more and more similar to Normal Distribution
	* it wont be exact and common fix is to adjust average $\mu = \mu - 0.5$ 
	* rule of the thumb is that we need at least 10 successes and 10 failures for binoma, so $np \geq 10$ and $n(1-p) \geq 10$
