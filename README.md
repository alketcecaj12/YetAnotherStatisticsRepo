# Yet Another Insignificant Statistics Note

In data science, hypothesis testing is a fundamental part of statistical analysis, used to make inferences or draw conclusions about populations based on sample data.

## This repo contains the most frequently used hypothesis tests in data science with use cases and Python code examples:

### Z-Test:

Used to determine if there is a significant difference between sample and population means.
Assumes the sample size is large (typically 𝑛>30 n>30) and data follows a normal distribution.

### T-Test:
Used to compare the means of two groups.
Independent T-Test: Compares means from two different groups.
Paired T-Test: Compares means from the same group at different times.
One-Sample T-Test: Compares the mean of a single group against a known mean.

### Chi-Square Test:

Used for categorical data to assess how likely it is that an observed distribution is due to chance.
Chi-Square Goodness of Fit Test: Determines if a sample matches the population.
Chi-Square Test for Independence: Determines if there is an association between two categorical variables.

### ANOVA (Analysis of Variance):

Used to compare means among three or more groups.
One-Way ANOVA: Tests differences between groups based on one independent variable.
Two-Way ANOVA: Tests differences based on two independent variables.

### F-Test:

Used to compare two variances to see if they come from populations with equal variances.
Often used in conjunction with ANOVA.

### Mann-Whitney U Test:

A non-parametric test used to compare differences between two independent groups when the sample distributions are not normally distributed.

### Wilcoxon Signed-Rank Test:

A non-parametric test used for comparing two paired samples or repeated measurements on a single sample.

### Kruskal-Wallis Test:

A non-parametric version of ANOVA, used for comparing three or more groups.

### Pearson Correlation Coefficient Test:

Measures the strength and direction of the linear relationship between two continuous variables.

### Spearman Rank Correlation Test:

A non-parametric test that assesses how well the relationship between two variables can be described using a monotonic function.

### Log-Rank Test:

Used to compare the survival distributions of two samples.
