# ML 

### Why we do not use R^2 for the logistic regression?
https://stats.stackexchange.com/questions/328874/can-i-squareroot-r2-to-get-r-in-a-logistic-regression



## type 1 type2 error 
1. accept the null h when incorrect. 
2.  reject when null is correct.


## F partial
A partial F-test is an incremental F-test which is used to determine the statistical significance of a group of variables. It is based on two best-fit regression models. It determines the effect of extra variables on the explanatory power by the inclusion of the variables in the equation. It determines the better sign of the full model than the reduced model.

Requirements for partial F-test:

1. A full regression model in which all the variables of interest are included.

2. A reduced regression model in which all the variables are included except the variables which are required to be tested for statistical significance.

The formula for partial F-statistic:

The formula for partial F-statistic is defined as,

- image:  - https://www.chegg.com/homework-help/definitions/partial-f-statistic-31

## Cross-validation (statistics)
- https://en.wikipedia.org/wiki/Cross-validation_(statistics)

## overfitting and underfitting

- https://en.wikipedia.org/wiki/Overfitting



## Nuisance factor

- A nuisance factor is a factor that has some effect on the response, but is of no interest to the experimenter; however, the variability it transmits to the response needs to be minimized or explained

## There are 3*3=9 different combinations for each age groups (block). Since both main effects - emotion and alcohol consumption - have three levels, the size of each combination should be at least 12 for a sample with power 0.8 and effect size 0.4, resulting in a total of 2*3*3*12=216 samples.```
pwr.anova.test(k=9,f=0.4,sig.level = 0.05, power = 0.8)
n is number in each group here 11.32

```

## type 1 type 2 erros

- Type I and type II errors. ... In statistical hypothesis testing, a type I error is the rejection of a true null hypothesis (also known as a "false positive" finding), while a type II error is the failure to reject a false null hypothesis (also known as a "false negative" finding).


## F test 

- An F-test is any statistical test in which the test statistic has an F-distribution under the null hypothesis. It is most often used when comparing statistical models that have been fitted to a data set, in order to identify the model that best fits the population from which the data were sampled. Exact "F-tests" mainly arise when the models have been fitted to the data using least squares. The name was coined by George W. Snedecor, in honour of Sir Ronald A. Fisher. Fisher initially developed the statistic as the variance ratio in the 1920s.[1]


## leverage not necessarily to be outliers

## interaction plot 
interaction.plot(alchhol, mental, afer1)

## tukey's test

-  The Tukey Test (or Tukey procedure), also called Tukey’s Honest Significant Difference test, is a post-hoc test based on the studentized range distribution. An ANOVA test can tell you if your results are significant overall, but it won’t tell you exactly where those differences lie. After you have run an ANOVA and found significant results, then you can run Tukey’s HSD to find out which specific groups’s means (compared with each other) are different. The test compares all possible pairs of means.

To test all pairwise comparisons among means using the Tukey HSD, calculate HSD for each pair of means using the following formula:

- Assumptions for the test
Observations are independent within and among groups.
The groups for each mean in the test are normally distributed.
There is equal within-group variance across the groups associated with each mean in the test (homogeneity of variance).

- https://www.statisticshowto.datasciencecentral.com/tukey-test-honest-significant-difference/


# Out-of-bag error
- https://en.wikipedia.org/wiki/Out-of-bag_error

- Bootstrap aggregating, also called bagging, is a machine learning ensemble meta-algorithm designed to improve the stability and accuracy of machine learning algorithms used in statistical classification and regression. It also reduces variance and helps to avoid overfitting. Although it is usually applied to decision tree methods, it can be used with any type of method. Bagging is a special case of the model averaging approach.