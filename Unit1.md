Book to look at <https://www.openintro.org/stat/textbook.php>

# Unit 1

##Variables

Types of Variables:

* numerical (quantitative)
	* continuous
	* discrete
* categorical
	* ordinal
	* regular

Correlation does not imply causation, there is always possible that confounding variable exist. In order to study we need to first collect data by:
* observing
	* retrospective
	* prospective
* experiments

##Sampling

Sampling make it possible for us to exploratory analysis on smaller set. We need to make sure that sample is representatives of whole population.
Sampling biases:

* convenience sample
* non-response bias
* voluntary response bias
	* only ppl with strong opinions will vote

How we should collect data then?

* simple random sampling
* stratified sampling
	* we create strata (homogeneous groups, divided into category) and then randomly sample from those clusters
* cluster sampling
	* we divide into clusters and then randomly sample from some of those clusters
	* clusters are not homogeneous but are similar to each other
	* usually done for economical cost

##Experimental design

Principles:

* control
* randomise
* replicate
* block
	* block (split using) variables that are likely to affect the results
	* blocking is like stratifying
	* explanatory variables are conditions we can impose on experimental units, and are NOT block!


Random assignment and random sampling offer both causal and generalisation. Most experiments include volunteers so no generalisation is possible.

## Plots
We tend to put explanatory variables on x and response on y. We only talk about correlation not causation between two variables. When we evaluate relationship we look at:

* direction (positive/negative)
* shape (linear or other)
* strength (how much scatter?)
* out-layers
	* we should usually carefully consider all out-layers

Types of plots:

* scatter
* histogram
	* good for data density
	* data distribution
	* shapes
		* modality (unimodal, bi-modal, multi-modal, unformed)
		* bin width is also important
* dotplot
* boxplot
	* can't determine modality
* intensity map
* mosaic plot
	* combine relative freq  bar plot with marginal distribution

##Robust statistics	

Median and IQR is robust to outliers. Sometimes we prefer to transform data so we can plot it properly. Most popular:

* log
* sqr
* reverse (1/n)

We we do it:

* we want to see data differently
* we want to reduce skew
* strengthen non-linear relationship in scatter plot 

##Testing

H_0 represent our status quo while H_A represent our research question. We need to prove that H_A is more likely (reject H0)