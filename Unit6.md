# Unit 6 -  Introduction to linear regression

#Linear Correlation

* swapping axis does not make difference
* correlation coefficient is unitless and it is not affected by change of units
* sensitive to outliers
* residuals are defined as $e_i =  y_i - \hat{y_i}$ as data = fit + residuals
* if we want to fit the line
	* slope $b_1 = \frac{S_y}{S_x}R$
	* intercept $b_0  = \bar{ y } -b_1\bar{ x }$
	* intercept point will always pass through the middle of the data
* L2 is LS
* L1 is abs values
* be careful with extrapolation
* conditions for linear regression
	* linearity - use residual plots
	* near normal residuals - histogram + QQ plot
	* constant variability (homoscedasticity) - residual plots
* R^2 - what % of model is explained by response variable

#Regression with categorise variables

* one of the will be base value (==0)
* we estimate values as intercept + estimate4variable1 +estimate4variable2 + ...


#Out-layer

* out layers are point away from the cloud of points
* if they fall horizontal and don't influence the slope of regression line are leverage points
* one that influence the slope line are called influential points
	* its worth to take influential points out
	* don't act blind, think why you take them out
	* influential points might increase R-squared - always view the plot !

#inference for linear regression

* hypothesis - is the explanatory variable a significant predictor of the variable
	* Hypotheses are always about parameters (not point estimates) and subscript 0 refers to the intercept and 1 refers to the slope.
	* $H_0 = \beta_1$ and $H_A = \beta_1 \neq 0$ as we test for **any** relationship between explanatory and response variables
	* we use t statistics $T = \frac{b_1-0}{SE_{b1}}$ and $df = n -2$
		* abs(qt(1-0.5*ConfidenceInterval,df-2)) so for 95% and df=27 qt(0.975,25)
	* confidence interval is $b_1 \pm t^*_{df}SE_{b1}$
	* statistical inference is meaningless if you already have population data
	* inference on the intercept is rarely done
	* partitioning variability in y to explained and unexplained variability require analysis of variance (ANOVA)

#Variability Partitioning

* In ANOVA F statistics for the linear model is the ratio of explained to unexplained variability


