Unit 7 -  Multiple linear regressions
====================================

We have a set of numerical and categorical explanatory variables (multiple predictors) and want to  predict explanatory variable.

* any binary values (example shown hardcover and softcover books) will have the same slope (liner model)
	* if this is not the case we have to consider using interaction variables instead
* we have to assume that out explanatory variable have the same beh

#Adjusted R^2

* R2 will never decrease when a predictor is added to a linear model.
* $R^2 = \frac{\text{explained variability}}{\text{total variability}} so % of variability not explained is residuals
* therefore R^2 it will increase for every variable we add to compensate we use equation $R^2_{adj} = 1 - \frac{SSE}{SST}\frac{n-1}{n-k-1}	$, where k is no of predictors and n is model size
* Adjusted R2 tells us the percentage of variability in the response variable explained by the model, with a penalty for the number of predictors included in the model.

# Collinearity and parsimony

* predictors (independent variables) are collinear when they are correlated with each other
	* they should be independent!
	* Correlation of predictors
* parsimonious model - the simplest model, without predictors associated with each other
	* similar logic to Occam's razor
	* experiments are usually designed to control for collaborated restrictions

# Inference

Our hypothesis is that none of the exploratory variables are good predictors , $H_0 = \beta_1 = \beta_2 = ... = = \beta_k = 0$.
* Alternative is that at least one is ($\beta_i \neq 0$). This is what p-value of our model going to tell us.
* We will use t-statistics to test for slope with $df =  n-k-1$
* Confidence interval can be estimated from t-stats

##Model selection

* Stepwise model selection
	* In backwards model selection using adjusted R2 as the criterion, we drop variables from the model, one at a time, until adjusted R2 is maximized.
	* In backwards elimination model selection using p-value as the criterion, we start with the full model, and drop the variable with highest p-value, one at a time, until all the variables in the model are significant given the others.
	* We can’t drop individual levels of a variable, and since at least one level of race is significant, we keep the whole variable in.
	* in forward selection model we start with single var and add one by one until we got parsimonious model
	* as criteria we use:
		* adjusted R^2 for each model - we are interested in more reliable predictions
		* p-value from lm - we are interested in more significant predictors
			* it is used more commonly as it require fitting fewer models
		* expert opinion
		* AIC
		* BIC
		* DIC
		* Bayes factor
		* Mallow's Cp

##Conditions for MLR

* linear relationship between numerical variables x and y
	* random pattern in the residuals plot
* constant variability if residuals
	* plot residuals vs predicted
* independent residuals
	* no time structure
	* Sample size > 30 is useful for nearly normal sampling distribution of the mean in cases where the population distribution is not normal, however it has nothing to do with independence of observations.