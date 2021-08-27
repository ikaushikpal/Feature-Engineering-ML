# Why missing data is a concern?

Missing data can create major risk of producing incorrect conclusions due to absence of relevant information leading to invalid results.

Results of any statistical analysis used can be only as good as the quality of the data.
missing data arises for many reasons such as non-response, lost data, or skip patterns in surveys.


# Let us familiarize what are the most common types of missing data.
<div style="text-align:center"><img src="https://media-exp1.licdn.com/dms/image/C5612AQEiinc0uhEEJQ/article-inline_image-shrink_1000_1488/0/1532846117102?e=1635379200&v=beta&t=30Cig7ZUksRZ0zYQ4ERvIBCE4TeqMPVTqtmoTX1gtLc" /></div>


# Missing Completely at Random (MCAR)
___

Missing completely at random (MCAR) analysis assumes that missingness is unrelated of any unobserved data (response and covariate), meaning that the probability of a missing data value is independent of any observation in the data set.

In this case, missing and observed observations are generated from the same distribution, means there is no systematic mechanism that makes the data to be missing more than others. when this assumption is confirmed, you can perform a complete case(CC) analysis on the observed data.

MCAR produces reliable estimates that are unbiased but still there is a loss power due to poor design but not due to absence of the data.
___

If the probability of being missing is the same for all cases, then the data are said to be missing completely at random (MCAR). This effectively implies that causes of the missing data are unrelated to the data. We may consequently ignore many of the complexities that arise because data are missing, apart from the obvious loss of information. An example of MCAR is a weighing scale that ran out of batteries. Some of the data will be missing simply because of bad luck. Another example is when we take a random sample of a population, where each member has the same chance of being included in the sample. The (unobserved) data of members in the population that were not included in the sample are MCAR. While convenient, MCAR is often unrealistic for the data at hand.


# Missing At Random (MAR).
___
Consider the following example.

men are more likely to tell you their age than women
men are more likely to tell you their weight than women.
men are more likely to dropout in clinical trials than women.
 men are less likely to fill in a depression survey but this has nothing to do with their level of depression, after accounting for maleness.
familiar right? this is kind of missing is referred as missing at random. missing data at random(MAR) is more common than missing completely at random(MCAR) in all disciplines.

In this case, clearly the missing and observed observations are no longer coming from the same distribution and this is a crucial distinction between the two methods
___

If the probability of being missing is the same only within groups defined by the observed data, then the data are missing at random (MAR). MAR is a much broader class than MCAR. For example, when placed on a soft surface, a weighing scale may produce more missing values than when placed on a hard surface. Such data are thus not MCAR. If, however, we know surface type and if we can assume MCAR within the type of surface, then the data are MAR. Another example of MAR is when we take a sample from a population, where the probability to be included depends on some known property. MAR is more general and more realistic than MCAR. Modern missing data methods generally start from the MAR assumption.


# Missing Not at Random (MNAR)
___
For example, when most of the missing people from work are sickest people, people with the lowest education are missing on education, this kind of missing is referred as Missing Not at Random (MNAR).

MNAR analysis are problematic because the distribution of the missing observations do not only depend on the observed values but also the unobserved values as well. and in this case there is no need to model the random part and can be easily ignored.

What are statistical methods to handle missing data.

Multiple imputation and maximum likelihood (ML) are commonly used to deal with missing data and they both assume that at least the missing is at random and can not be ignored in the modeling process( big NO MNAR).
___

If neither MCAR nor MAR holds, then we speak of missing not at random (MNAR). In the literature one can also find the term NMAR (not missing at random) for the same concept. MNAR means that the probability of being missing varies for reasons that are unknown to us. For example, the weighing scale mechanism may wear out over time, producing more missing data as time progresses, but we may fail to note this. If the heavier objects are measured later in time, then we obtain a distribution of the measurements that will be distorted. MNAR includes the possibility that the scale produces more missing values for the heavier objects (as above), a situation that might be difficult to recognize and handle. An example of MNAR in public opinion research occurs if those with weaker opinions respond less often. MNAR is the most complex case. Strategies to handle MNAR are to find more data about the causes for the missingness, or to perform what-if analyses to see how sensitive the results are under various scenarios.

# Best practices to prevent missing data
___
The following are the most effective way of handling missing data.

“Good design may not eliminate the problem of missing data, but … it can reduce it, so that the modern analytic machinery can be used to extract statistical meaning from study data. Conversely, we note that when insufficient attention is paid to missing data at the design stage, it may lead to inferential problems that are impossible to resolve in the statistical analysis phase.” —Lavori, et al. (2008)
Reduce Missing Data Through Minimizing Dropouts
Points to remember!

Under MCAR analysis, you can analyze the observed observation and ignore discard any missing observations.
MCAR assumptions not hold then using complete case(CC) analysis produces bias results.