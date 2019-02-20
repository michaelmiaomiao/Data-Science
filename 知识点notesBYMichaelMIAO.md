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


## There are other models such as XGBoost that we did not try and combining predictions from other models can also improve the accuracy.


## Bootstrapping (statistics)
- https://en.wikipedia.org/wiki/Bootstrapping_(statistics)

## supervise and unsupervised learnaing

- https://machinelearningmastery.com/supervised-and-unsupervised-machine-learning-algorithms/



## lda qda classification 

- https://scikit-learn.org/stable/auto_examples/classification/plot_lda_qda.html

- When the classes are well-separated, the parameter estimates for the logistic model are surprisingly unstable. LDA does not suffer from this.
If n is small and the distribution of the predictors X is approximately normal in each of the classes, the LDA model is more stable than logistic.
For these reasons, and some others, LDA is the preferred method when dealing with > 2 response classes.
The LDA classifier assumes that each class comes from a normal distribution with a class-specific mean vector and a common variance. We utilize LDA to estimate the parameters so that we can leverage the Bayes classifier. The Bayes classifier is a simple and highly effective classifier that assigns each observation to the most likely class given its predictor values. The Bayes classifier has the lowest possible error rate out of all classifiers if the terms are correctly specified. Thus LDA is a classifier that attempts to approximate the Bayes classifier.

- The difference is really a bias-variance trade-off. With p predictors, estimating a co variance matrix requires estimating p(p+1)/2 parameters. The QDA estimates a separate co variance matrix for each class, so as the number of predictors becomes high, we experience a computational expense. Conversely, if we assume a common co variance matrix, we only have to do the computation once. LDA is a much less flexible classifier, than QDA, thus has substantially lower variance. However, if the assumption of uniform variance is highly off, then LDA can suffer high bias. In general, LDA tends to be better than QDA if there are relatively few training observations, so therefore reducing variance is crucial. QDA is recommended if the training set is very large, so that the variance of the classifier is not a major concern.

Between Logistic regression LDA and QDA, the biggest things to take into consideration are the type of decision boundary that is required. If highly linear, than LDA and Logistic may prove superior, if non-linear, the edge may be given to QDA. Though keep in mind we can do simple transformations to take non-linearity into consideration with Logistic models, similar to how we did in linear regression.