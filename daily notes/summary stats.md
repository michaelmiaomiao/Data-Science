# Statistics Knoledge Colledted.

## for data sicence level
--
  
- [source for data used ](https://drive.google.com/drive/folders/0B98qpkK5EJemYnJ1ajA1ZVJwMzg)
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
- #Explore the data analysis 

	- data type structure / unstrucure.
	- ordinary is one type of ordered factor categorial data.
	- data: continous, discrete, categorical(binary, ordinal.)
	- database are more detaield in their classification of data types [sql learning](https://www.w3schools.com/sql/sql_datatypes.asp)
	- rectangualar data -- data frame
	- python uses panda libratry `DataFrame()` 
	-  index created by default
	-  R uses `data.frame`
	-  R does not suupor use-sepecidied indexes , pyton does
	-  non-rec data: times series data, spatial data for ammping and location analytics, knowledge graph(network optimization and reccomnederssystmens)
	-  we care more about rec data - pred model.

- #Estimation of location
	- mean , weightedmeanm, median, weighted median, trimmed mean, robust [robust]() not sensitive to extrene valuesm outliers. 
	- data science and ba refer estimated for calues to draw actual and therotical as **METRIC**
	- Trimmed minus the extreme values's counts when doing mean
	- weighted  x* w / w sigma
	- mean is more sensitive to data, but median is less likely to be affected.
	- median is not only robust estimate, trimmed mean, eg 10% top and buttom in real life. -- compromise for median and mean.
	- others more robust
	- [good sources slides for calculation estimate ](http://www.stat.purdue.edu/~mlevins/courses/STAT%20511/index.html)
	- [king of ds](https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=76429)

- #Esitimate of variablity 
	- Deviations :  differnece obs - estimate location. = errors = residuals. （残差）
	- variance : sum of squared deviations from mean divied by n-1 = mean squaired errors.
	- stanadard deviance: suqiree root of variances -- euclidean norm
	- MAD: mean abs of dev
	- range 
	- ranks : metriecs based on data values from low to high.
	- percentile 
	- inrerquantile range. = IQR
	-  MAD= x - xi / n
	-  var = s^2 = (x- xi)^2 / n-1
	-  **degree of freedom** usually don't care, cuz n is large. (cue variable why n-1) _____ it is on premise that you want make estimate of pop based on samp. 
	-  n --- biased var. (underestimate the var)
	-  n - 1 standard non biased vstimate
	-  In fact:  consider constraints in computing estimates, n-1 === one constraint. [choosing K]
	-  **The above are not robost**
	-  STD > MAD >MEDIAN AD
	-  后俩基于 constraint scale of factor ，前者基于norm dist 

- #  Exploring thedata dist.
	- boxplot, freq.table, hist, density, 
	

- # Exploring binary and cate. data. 

	- mode, expected, bar chars, pie
	- bar chart similar to his. -- but x-axis not orderd.
	- *expected value = a form of weighted mean in which the weights are prob.*
	- cate data usually summarised in proportion
	- distinct thigns, levels of fa, binned num.

- # Correlation
	- modelling 
	- predict and target 
	- coefficient correlation -- numerica 1 -1 
	- correlation matrix
	- cc = 0 means no assoication
	- contingency tables, hexagonal binning, contour plots, volin
	- denssity 
	- two categorial table 
> > 	**- R size larger larger R so adjuest R is preferred   
**
- # data and smapling dist. 
	-sample, population, n, rs, strata, sample bias. 
	- data quality matters here
	- bias -- statistical bias to measurements of sampling erroes systemic and proces when coolec
	- observable or not 
	- Ramdom selection -- avoid bis 
	- in stratigied sampling 
	- size matter 
	- central limist therom
	- standard error = se = s/ root of n
	- standard deviation measures variability of individual data points
	- while stand error measure the variability of the sampling metric.
	- the lrger the sample size the normally it is 
	- dist. of sample are normally sgagoed 
	- error , standardzize by dividing sde. 根号下
	- z-scoe of standarlizing an indiviual pooint
	- errors are normally dist. usually while data might not.
	- possion dist. for per time period 
- # t dist. estimate of mean
	- degree of freedom
	- n sample size 
	- t is similiar to z but thihcker tails for sampleing.
	- t used for sample mean, regression parameters and more. 


- # binomial dist.
	- tirl, sucess, 
	-  n 变大的时候 可以被 normal approximate
	-  n * p(1-p)
- # Poisson dist. 
	- Many processes produce events randomly at a given overall rate.
	- lamba-  rate which occurs events
	- position frequency distr. given time unit
	- exponential dis.**the time or distance from one even to another**
	- weibull dist. version of expo rate is allowed to shift over time.


- # statistical experiments and siinificace testing.
	- pm uses alot 
	- interferce 
	- limitted sample to larger population
	- formualte the hyphthesis ---- design experince ---- collet data ---- inference and conclusion
	- typical hp : a treatment is better than control

- # ab testing 
	- treatment 
	- traetment group
	- control group
	- randamization 
	- susbjects
	- test statistics
	- eg: seed germination for product, profit, produces more clickm, web ads conversisions
	- bliing study / double blind


- # hypo

	- why hupothesis ? 1. mis understadnd a random evens as a pattern thing. 2. failure to anticipate extreme
	- mean difference is more extreme or not.
	

- # resampling
	- resampling helps with ml algorithm.
	- **two types: bootstrap(with repalcement) / permutation(random test) **
	- permutation : combine results from different groups; shufffle and randomnly draw with NO replacementof sae size as group A; repeat that with size equals to group B *with remianing  data*; C,D,E, if any; calculate the stats and constitues one permutation iteration; repeart R times to form a permutation dist. if the overseved difference lies out side most of the permuation distribution, than we conclude that chance is not reponsible. 
	- 


- # statsi sig and p-value
	- 	P-value: the prob. of obtaiing reuslts as unsuall or extme
	-  al[ha unsual 
	-  type 1 reject when h0 true
	-  type 2 accpet when h0 falls
	- **pvalue** is the prob. that the result is due to chance. 
	- The p-value is the smallest level of significance at which we can still reject the null hypothesis, given the observed sample statistic
	- It is the prob. given a chance model, results as extreme as the observed results could occur.
	- pvalue < alpha leads to reject null hypothessis.
	- t test
	- overfitting - fititng to the noise

- # anova 
	- pairwise 
	- F statistics 
	- SS sum of square 
	- based on the ratio of variance by group means
	- ms(treatment) / me(error) gievs f statistics
	- For illustration, suppose that you wish to test the hypothesis that 𝑝
p
 coefficients are zero, and thus these variables can be omitted from the model, and you also have 𝑘
k
 coefficients in

- # CHi-squ  !!!
	- CHIsquare stat == measure of extend to whcih some observed data departs from expectation
	- df 
	- pearson residual = obs - exp / root of exp
	- (r-1)(c-1)
	- shuttle resampling test 
	- chi-squre!!! more as a filter to determine effectr or feature is wortht of further consideration than as a formal test of signiicance. 
	- **feature selection** in machine larning
	- chi which assumeption of independence.
	
- # power and sample
	- efffect size
	- power 
	- sigifican level


- # reg.
	- fitted values -- estimate y head
	- resi -- difference obs - fitted.=== errors
	- yi = b0+b1x+ei
	- yihead = b0head +b1heardx
	- rss residual sum
	- regr ---- predict / explain
	- r-suqare == the proportion of variance explained by model
	- t= b/ se error of coefficient 
	- higher t, lowewr pvalue means significant
	- minimize AIC BIC from bayesian
	- weighted reg 1 inverser-variance weight
	- RMSE / Rsuqare 最重要俩指标
	- stanadarlized error of coefficent can be used to measure the reliabitlity of the variable contributin to a model.
	- factor used: dummy 0-1
	- factors needed to be converted to numeric in use.
	- confounding variable 
	- cooked distance -- lever+ residual size

- # classi
	- naive bayesian 查查
	- bay for numdeic needs :1 bind and conver to cate, 2 prob. model p(x|y=i)
	- discrininat analysi : LDA taelss measure of importanace and 好计算
	- lda believes the covarince matrix same for groups e covariance matrix:
	- **LOGIST TIC** 查查


- # evalue model 
  	- accuracy 
  	- confusion matrix 看图
  	- sebsitivity = percent of 1s cirreckt classfie 
  	- bagging resample records
  	- rf bag+ resample variables
  	- boosting requires more care and tune.: give weights to the record with large residual
  	- regularization : add penalty term besed on number of parameters in model to avoid overffting
# boosting
- Boosting Trees
Reassign weights to samples based on the results of previous iterations of classifications.
Harder to classify points get weighted more. Iterative algorithm where each execution is based on the previous results.

# RF
- Random Forest
RF applies bootstrap aggregation to train many different trees.
This creates an ensemble of different individual decision trees 
- In random forest algorithm, Instead of using information gain or gini index for calculating the root node, the process of finding the root node and splitting the feature nodes will happen randomly. 



 
 - # Unsupervised learning
  	- principal component: lienar combination of the predictor vaeibels 查查
  	- http://support.minitab.com/en-us/minitab/17/topic-library/modeling-statistics/multivariate/principal-components-and-factor-analysis/what-is-pca/
  	- loading : weights that trasnform the predictors into the components

  	
  	
  - #  (Redirected from Ridge regression)
  - lasso set coe === zero , while ridge not
  - least absolute shrinkage and selection operator

  

----------------------------------------------------
-----------------------------------------------------				

# bayesian :
- http://uc-r.github.io/naive_bayes
his is primarily because what is usually needed is not a propensity (exact posterior probability) for each record that is accurate in absolute terms but just a reasonably accurate rank ordering of propensities.

# decision tree
- Advantages of Decision Trees
Very easy to interpret and understand
Works on both continuous and categorical features
No normalization or scaling necessary
Prediction algorithm runs very fast


# Gini index
Gini index: Mainly used with tree-based methods and commonly referred to as a measure of purity where a small value indicates that a node contains predominantly observations from a single class. Objective: minimize

# Gini importance

Every time a split of a node is made on variable m the gini impurity criterion for the two descendent nodes is less than the parent node. Adding up the gini decreases for each individual variable over all trees in the forest gives a fast variable importance that is often very consistent with the permutation importance measure.



# collinearity
- A simple way to detect collinearity is to look at the correlation matrix of the predictors. An element of this matrix that is large in absolute value indicates a pair of hig

# auc
- AUC - ROC curve is a performance measurement for classification problem at various thresholds settings. ROC is a probability curve and AUC represents degree or measure of separability. It tells how much model is capable of distinguishing between classes. Higher the AUC, better the model is at predicting 0s as 0s and 1s as 1s. By analogy, Higher the AUC, better the model is at distinguishing between patients with disease and no disease.

# roc 
- The ROC is also known as a relative operating characteristic curve, because it is a comparison of two operating characteristics (TPR and FPR) as the criterion changes.[8]


# Leave-one-out cross-validation

- Filter methods are generally used as a preprocessing step. The selection of features is independent of any machine learning algorithms. Instead, features are selected on the basis of their scores in various statistical tests for their correlation with the outcome variable. The correlation is a subjective term here. For basic guidance, you can refer to the following table for defining correlation co-efficients.

fs1

Pearson’s Correlation: It is used as a measure for quantifying linear dependence between two continuous variables X and Y. Its value varies from -1 to +1. Pearson’s correlation is given as:
fs2

LDA: Linear discriminant analysis is used to find a linear combination of features that characterizes or separates two or more classes (or levels) of a categorical variable.
ANOVA: ANOVA stands for Analysis of variance. It is similar to LDA except for the fact that it is operated using one or more categorical independent features and one continuous dependent feature. It provides a statistical test of whether the means of several groups are equal or not.
Chi-Square: It is a is a statistical test applied to the groups of categorical features to evaluate the likelihood of correlation or association between them using their frequency distribution.


看看 如何 logistc odds之类的
 sensititivy and specificity
 knn


# model tranfer
- https://newonlinecourses.science.psu.edu/stat501/node/320/


# Variance Inflation Factors (VIF)
- VIF > 10 is considered solid evidence of multicollinearity.



#chi 
A chi-squared test, also written as χ2 test, is any statistical hypothesis test where the sampling distribution of the test statistic is a chi-squared distribution when the null hypothesis is true. Without other qualification, 'chi-squared test' often is used as short for Pearson's chi-squared test. The chi-squared test is used to determine whether there is a significant difference between the expected frequencies and the observed frequencies in one or more categories.

# PCA和LDA（linear discriminant analysis）都可以用来减少feature。PCA保留variation最大的feature，LDA保留对于结果最容易进行分类的feature。




My name is JIASHU MIAO and im currently a third year student at ucla double majors in math of computation and staistics. These two majors are a actually a great overlap which contains knowledge of mathematics, statistics and programming and scripting langugaes. The combined study occupies necessary basics for data science and I also get many past experince working as an intern or lab assistant in the fields of data analysis in different indusstris like healthcare, biomedicine, educatoinal it company and financial service. I like data science and never feel that involves so many topics.

RAM



# database optimization
- probr index
- rettrive relevant data
- getting rid of corredlate subs
- avoid coding loops 
- Penalized Least Squares
L1 (LASSO)
L2 (Ridge)


# SVM- 
Describe how the support vector machine (SVM) algorithm works.
**SVM attempt to find a hyperplane that separates classes by maximizing the margin**
- *https://docs.google.com/presentation/d/1VvSWus6sjXEV7WG7FuH__Pi5rwB0_WlKc7A5Whx5gVg/edit#slide=id.g289adf6022_0_115* SOURCE HERE.
- SVMs can employ the kernel trick which can map linear non-separable inputs into a higher dimension where they become more easily separable. 


# Many ways to attempt to fix overfitting
- **Increase Training Data Size
Regularization
Early Stopping
K-Fold Cross Validation**

# AC
Accuracy is simply a ratio of correctly predicted observation to the total observations. Accuracy is a useful measure but only when you have symmetric datasets where values of false positive and false negatives are almost same. Therefore, we need to also consider Precision and Recall.
Accuracy =  ( TP+TN ) / ( TP+FP+FN+TN)

#PC
Precision is the ratio of correctly predicted positive observations to the total predicted positive observations. The question that this metric answer is of all points that labeled as positive, how many were actually positive?
Precision = TP / (TP+FP)

#RECALL
Recall (Sensitivity) is the ratio of correctly predicted positive observations to the all observations in actual class.
Recall = TP / (TP+FN)

### What metrics can be used to evaluate a regression task?
!!!!
Mean Absolute Error (MAE) is the mean of the absolute value of the errors:
Mean Squared Error (MSE) is the mean of the squared errors: **BETTER PUNISHES LARGER ERRORS**
Root Mean Squared Error (RMSE) is the square root of the mean of the squared errors: **EVEN BETTER BECAUSE RMSE y unists is **


# intuitive ab 
- https://www.optimizely.com/optimization-glossary/ab-testing/


- If you know the true mean of your population from which you sampled, you can take samples of your sample multiple times and check if the mean of these samples are normally distributed around the true mean of the population.
- With multiple hypotheses test you increase the likelihood of a rare event occurring, meaning you need to adjust your alpha value you use to compare your p-value against for significance accordingly. 

- Since this is a multiple inference problem you can correct your alpha value using the Bonferroni correction method.

- Adaptive Experiment Design
This type of approach is also sometimes known as Bandit Selection.
Keep in mind it becomes harder to clearly evaluate as the experiment is changing.

#power
The power of any test of statistical significance is defined as the probability that it will reject a false null hypothesis.
Statistical power is inversely related to beta or the probability of making a Type II error. In short, power = 1 – β.
- afected by effectsize 
- comparing pvalue with type 1
- If we set a larger α we then in turn allow for larger p-values to be considered significant, meaning we increase the power of the test.  

# cate
- There are two qualitative levels: nominal and ordinal. The nominal level represents categories that cannot be put in any order, while ordinal represents categories that can be ordered.
- The Pareto diagram is a special type of bar chart where the categories are shown in descending order of frequency, and a separate curve shows the cumulative frequency.

# covariance
- Covariance is a measure of the joint variability of two variables.
➢ A positive covariance means that the two variables move together.
➢ A covariance of 0 means that the two variables are independent.
➢ A negative covariance means that the two variables move in opposite directions.

- Correlation is a measure of the joint variability of two variables. Unlike covariance, correlation could be thought of as a standardized measure. It takes on values between -1 and 1, thus it is easy for us to interpret the result.
- ➢ A correlation of 1, known as perfect positive correlation, means that one variable is perfectly explained by the other.
➢ A correlation of 0 means that the variables are independent.
➢ A correlation of -1, known as perfect negative correlation, means that one variable is explaining the other one
perfectly, but they move in opposite directions.

# Biology. Most biological measures are normally distributed, such as: height; length of arms, legs, nails; blood pressure; thickness of tree barks, etc.

# t test 本质
- All else equal, the Student’s T distribution has fatter tails than the Normal distribution and a lower peak. This is to reflect the higher level of uncertainty, caused by the small sample size.
 The p-value is the smallest level of significance at which we can still reject the null hypothesis, given the observed sample statisticpa


# pca 是l2 which is ridge 就是 不把 系数为0 punish小

# transformation for model.
diagnostic plot

diagnostic plots
The first plot depicts residuals versus fitted values. Residuals are measured as follows:

residual =  observed y   –   model-predicted y

The plot of residuals versus predicted values is useful for checking the assumption of linearity and homoscedasticity. If the model does not meet the linear model assumption, we would expect to see residuals that are very large (big positive value or big negative value). To assess the assumption of linearity we want to ensure that the residuals are not too far away from 0 (standardized values less than -2 or greater than 2 are deemed problematic). To assess if the homoscedasticity assumption is met we look to make sure that there is no pattern in the residuals and that they are equally spread around the y = 0 line.

The tests and intervals estimated in summary(lm3) are based on the assumption of normality. The normality assumption is evaluated based on the residuals and can be evaluated using a **QQ-plot** (plot 2) by comparing the residuals to "ideal" normal observations. Observations lie well along the 45-degree line in the QQ-plot, so we may assume that normality holds here.

The third plot is a scale-location plot (square rooted standardized residual vs. predicted value). This is useful for checking the assumption of homoscedasticity. In this particular plot we are checking to see if there is a pattern in the residuals.

The assumption of a random sample and independent observations cannot be tested with diagnostic plots. It is an assumption that you can test by examining the study design.

The fourth plot is of "Cook's distance", which is a measure of the influence of each observation on the regression coefficients. The Cook's distance statistic is a measure, for each observation in turn, of the extent of change in model estimates when that particular observation is omitted. Any observation for which the Cook's distance is close to 1 or more, or that is substantially larger than other Cook's distances (highly influential data points), requires investigation.

Outliers may or may not be influential points. Influential outliers are of the greatest concern. They should never be disregarded. Careful scrutiny of the original data may reveal an error in data entry that can be corrected. If they remain excluded from the final fitted model, they must be noted in the final report or paper.


# Optimization in statistics
- In a statistical context the decision variable will usually be the paramaters of a model, and f either the model likelihood to be maximized or a measure of discrepancy between data and predictions which is to be minimized.
- 
- Statistical examples are:
	- Maximum likelihood estimator (MLE)
 	- Ordinary least squares (OLS)
 

# randomization
When we use a randomization approach, we permute the Y values, while holding the X values constant. For example, if the original data were 

45 53 73 80
22 30 29 38
then three of our resamples might be

45  53  73  80
38  22  30  29

45  53  73  80
29  22  30  38

45  53  73  80
22  38  30  29

Notice how the top row always stays in the same order, while the bottom row is permuted randomly. This means that the expected value of the correlation between X and Y will be 0.00, not the correlation in the original sample.


# svm methods
construct AUROC and calculate AUC?


# what is VIP facror 



which is reguliazation 
lacoov or ridge




# Statistics Knoledge Colledted.

## for data sicence level
--
  
- [source for data used ](https://drive.google.com/drive/folders/0B98qpkK5EJemYnJ1ajA1ZVJwMzg)
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
- #Explore the data analysis 

	- data type structure / unstrucure.
	- ordinary is one type of ordered factor categorial data.
	- data: continous, discrete, categorical(binary, ordinal.)
	- database are more detaield in their classification of data types [sql learning](https://www.w3schools.com/sql/sql_datatypes.asp)
	- rectangualar data -- data frame
	- python uses panda libratry `DataFrame()` 
	-  index created by default
	-  R uses `data.frame`
	-  R does not suupor use-sepecidied indexes , pyton does
	-  non-rec data: times series data, spatial data for ammping and location analytics, knowledge graph(network optimization and reccomnederssystmens)
	-  we care more about rec data - pred model.

- #Estimation of location
	- mean , weightedmeanm, median, weighted median, trimmed mean, robust [robust]() not sensitive to extrene valuesm outliers. 
	- data science and ba refer estimated for calues to draw actual and therotical as **METRIC**
	- Trimmed minus the extreme values's counts when doing mean
	- weighted  x* w / w sigma
	- mean is more sensitive to data, but median is less likely to be affected.
	- median is not only robust estimate, trimmed mean, eg 10% top and buttom in real life. -- compromise for median and mean.
	- others more robust
	- [good sources slides for calculation estimate ](http://www.stat.purdue.edu/~mlevins/courses/STAT%20511/index.html)
	- [king of ds](https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=76429)

- #Esitimate of variablity 
	- Deviations :  differnece obs - estimate location. = errors = residuals. （残差）
	- variance : sum of squared deviations from mean divied by n-1 = mean squaired errors.
	- stanadard deviance: suqiree root of variances -- euclidean norm
	- MAD: mean abs of dev
	- range 
	- ranks : metriecs based on data values from low to high.
	- percentile 
	- inrerquantile range. = IQR
	-  MAD= x - xi / n
	-  var = s^2 = (x- xi)^2 / n-1
	-  **degree of freedom** usually don't care, cuz n is large. (cue variable why n-1) _____ it is on premise that you want make estimate of pop based on samp. 
	-  n --- biased var. (underestimate the var)
	-  n - 1 standard non biased vstimate
	-  In fact:  consider constraints in computing estimates, n-1 === one constraint. [choosing K]
	-  **The above are not robost**
	-  STD > MAD >MEDIAN AD
	-  后俩基于 constraint scale of factor ，前者基于norm dist 

- #  Exploring thedata dist.
	- boxplot, freq.table, hist, density, 
	

- # Exploring binary and cate. data. 

	- mode, expected, bar chars, pie
	- bar chart similar to his. -- but x-axis not orderd.
	- *expected value = a form of weighted mean in which the weights are prob.*
	- cate data usually summarised in proportion
	- distinct thigns, levels of fa, binned num.

- # Correlation
	- modelling 
	- predict and target 
	- coefficient correlation -- numerica 1 -1 
	- correlation matrix
	- cc = 0 means no assoication
	- contingency tables, hexagonal binning, contour plots, volin
	- denssity 
	- two categorial table 

- # data and smapling dist. 
	-sample, population, n, rs, strata, sample bias. 
	- data quality matters here
	- bias -- statistical bias to measurements of sampling erroes systemic and proces when coolec
	- observable or not 
	- Ramdom selection -- avoid bis 
	- in stratigied sampling 
	- size matter 
	- central limist therom
	- standard error = se = s/ root of n
	- standard deviation measures variability of individual data points
	- while stand error measure the variability of the sampling metric.
	- the lrger the sample size the normally it is 
	- dist. of sample are normally sgagoed 
	- error , standardzize by dividing sde. 根号下
	- z-scoe of standarlizing an indiviual pooint
	- errors are normally dist. usually while data might not.
	- possion dist. for per time period 
- # t dist. estimate of mean
	- degree of freedom
	- n sample size 
	- t is similiar to z but thihcker tails for sampleing.
	- t used for sample mean, regression parameters and more. 


- # binomial dist.
	- tirl, sucess, 
	-  n 变大的时候 可以被 normal approximate
	-  n * p(1-p)
- # Poisson dist. 
	- Many processes produce events randomly at a given overall rate.
	- lamba-  rate which occurs events
	- position frequency distr. given time unit
	- exponential dis.**the time or distance from one even to another**
	- weibull dist. version of expo rate is allowed to shift over time.


- # statistical experiments and siinificace testing.
	- pm uses alot 
	- interferce 
	- limitted sample to larger population
	- formualte the hyphthesis ---- design experince ---- collet data ---- inference and conclusion
	- typical hp : a treatment is better than control

- # ab testing 
	- treatment 
	- traetment group
	- control group
	- randamization 
	- susbjects
	- test statistics
	- eg: seed germination for product, profit, produces more clickm, web ads conversisions
	- bliing study / double blind


- # hypo

	- why hupothesis ? 1. mis understadnd a random evens as a pattern thing. 2. failure to anticipate extreme
	- mean difference is more extreme or not.
	

- # resampling
	- resampling helps with ml algorithm.
	- **two types: bootstrap(with repalcement) / permutation(random test) **
	- permutation : combine results from different groups; shufffle and randomnly draw with NO replacementof sae size as group A; repeat that with size equals to group B *with remianing  data*; C,D,E, if any; calculate the stats and constitues one permutation iteration; repeart R times to form a permutation dist. if the overseved difference lies out side most of the permuation distribution, than we conclude that chance is not reponsible. 
	- 


- # statsi sig and p-value
	- 	P-value: the prob. of obtaiing reuslts as unsuall or extme
	-  al[ha unsual 
	-  type 1 reject when h0 true
	-  type 2 accpet when h0 falls
	- **pvalue** is the prob. that the result is due to chance. 
	- It is the prob. given a chance model, results as extreme as the observed results could occur.
	- pvalue < alpha leads to reject null hypothessis.
	- t test
	- overfitting - fititng to the noise

- # anova 
	- pairwise 
	- F statistics 
	- SS sum of square 
	- based on the ratio of variance by group means
	- ms(treatment) / me(error) gievs f statistics
	- For illustration, suppose that you wish to test the hypothesis that 𝑝
p
 coefficients are zero, and thus these variables can be omitted from the model, and you also have 𝑘
k
 coefficients in

- # CHi-squ  !!!
	- CHIsquare stat == measure of extend to whcih some observed data departs from expectation
	- df 
	- pearson residual = obs - exp / root of exp
	- (r-1)(c-1)
	- shuttle resampling test 
	- chi-squre!!! more as a filter to determine effectr or feature is wortht of further consideration than as a formal test of signiicance. 
	- **feature selection** in machine larning
	- chi which assumeption of independence.
	
- # power and sample
	- efffect size
	- power 
	- sigifican level


- # reg.
	- fitted values -- estimate y head
	- resi -- difference obs - fitted.=== errors
	- yi = b0+b1x+ei
	- yihead = b0head +b1heardx
	- rss residual sum
	- regr ---- predict / explain
	- r-suqare == the proportion of variance explained by model
	- t= b/ se error of coefficient 
	- higher t, lowewr pvalue means significant
	- minimize AIC BIC from bayesian
	- weighted reg 1 inverser-variance weight
	- RMSE / Rsuqare 最重要俩指标
	- stanadarlized error of coefficent can be used to measure the reliabitlity of the variable contributin to a model.
	- factor used: dummy 0-1
	- factors needed to be converted to numeric in use.
	- confounding variable 
	- cooked distance -- lever+ residual size

- # classi
	- naive bayesian 查查
	- bay for numdeic needs :1 bind and conver to cate, 2 prob. model p(x|y=i)
	- discrininat analysi : LDA taelss measure of importanace and 好计算
	- lda believes the covarince matrix same for groups e covariance matrix:
	- **LOGIST TIC** 查查


- # evalue model 
  	- accuracy 
  	- confusion matrix 看图
  	- sebsitivity = percent of 1s cirreckt classfie 
  	- bagging resample records
  	- rf bag+ resample variables
  	- boosting requires more care and tune.: give weights to the record with large residual
  	- regularization : add penalty term besed on number of parameters in model to avoid overffting

 
 - # Unsupervised learning
  	- principal component: lienar combination of the predictor vaeibels 查查
  	- http://support.minitab.com/en-us/minitab/17/topic-library/modeling-statistics/multivariate/principal-components-and-factor-analysis/what-is-pca/
  	- loading : weights that trasnform the predictors into the compoonents

  	
  	
  - #  (Redirected from Ridge regression)
  - lasso set coe === zero , while ridge not
  - least absolute shrinkage and selection operator


# bayesian :
- http://uc-r.github.io/naive_bayes
his is primarily because what is usually needed is not a propensity (exact posterior probability) for each record that is accurate in absolute terms but just a reasonably accurate rank ordering of propensities.


#z Gini index: Mainly used with tree-based methods and commonly referred to as a measure of purity where a small value indicates that a node contains predominantly observations from a single class. Objective: minimize



# A simple way to detect collinearity is to look at the correlation matrix of the predictors. An element of this matrix that is large in absolute value indicates a pair of hig


# Leave-one-out cross-validation

- Filter methods are generally used as a preprocessing step. The selection of features is independent of any machine learning algorithms. Instead, features are selected on the basis of their scores in various statistical tests for their correlation with the outcome variable. The correlation is a subjective term here. For basic guidance, you can refer to the following table for defining correlation co-efficients.

fs1

Pearson’s Correlation: It is used as a measure for quantifying linear dependence between two continuous variables X and Y. Its value varies from -1 to +1. Pearson’s correlation is given as:
fs2

LDA: Linear discriminant analysis is used to find a linear combination of features that characterizes or separates two or more classes (or levels) of a categorical variable.
ANOVA: ANOVA stands for Analysis of variance. It is similar to LDA except for the fact that it is operated using one or more categorical independent features and one continuous dependent feature. It provides a statistical test of whether the means of several groups are equal or not.
Chi-Square: It is a is a statistical test applied to the groups of categorical features to evaluate the likelihood of correlation or association between them using their frequency distribution.


看看 如何 logistc odds之类的
 sensititivy and specificity
 knn


# model tranfer
- https://newonlinecourses.science.psu.edu/stat501/node/320/


# Variance Inflation Factors (VIF)


#chi 
A chi-squared test, also written as χ2 test, is any statistical hypothesis test where the sampling distribution of the test statistic is a chi-squared distribution when the null hypothesis is true. Without other qualification, 'chi-squared test' often is used as short for Pearson's chi-squared test. The chi-squared test is used to determine whether there is a significant difference between the expected frequencies and the observed frequencies in one or more categories.

# PCA和LDA（linear discriminant analysis）都可以用来减少feature。PCA保留variation最大的feature，LDA保留对于结果最容易进行分类的feature。




My name is JIASHU MIAO and im currently a third year student at ucla double majors in math of computation and staistics. These two majors are a actually a great overlap which contains knowledge of mathematics, statistics and programming and scripting langugaes. The combined study occupies necessary basics for data science and I also get many past experince working as an intern or lab assistant in the fields of data analysis in different indusstris like healthcare, biomedicine, educatoinal it company and financial service. I like data science and never feel that involves so many topics.

RAM



# database optimization
- probr index
- rettrive relevant data
- getting rid of corredlate subs
- avoid coding loops 





## experiment design 


- Quantitative Variables Discrete Variables Continuous Variables
Categorical Variables Nominal Variables Ordinal Variables

- **Sample covariance** is calculated by computing (signed) deviations of each measurement from the average of all measurements for that variable. Then the deviations for the two measurements are multiplied together sepa- rately for each subject. Finally these values are averaged (actually summed and divided by n-1, to keep the statistic unbiased). Note that the units on sample covariance are the products of the units of the two variables.
-  The general formula for sample covariance is 􏰆ni=1(xi −x ̄)(yi −y ̄)
Cov(X, Y ) = n − 1


## correlation coefficient 

- The correlation between two random variables is a number that runs from -1 through 0 to +1 and indicates a strong inverse relationship, no rela
- tionship, and a strong direct relationship, respectively.
- % variation in y can be explaine by.



## distributions 
- The binomial distribution 
- 
The multinomial distribution is a discrete distribution that can be used to model situations where a subject has n trials each of whi**ch independently can result in one of k different**

- The Poisson distribution is a discrete distribution whose support is the non- negative integers (0, 1, 2, . . .). Many measurements that represent counts which have no theoretical upper limit, such as the number of times a subject clicks on a moving target on a computer screen in one minute, follow a Poisson distribution.


- A chi-square distribution is a continuous distribution with support on the pos- itive real numbers whose family is indexed by a single “degrees of freedom” pa- rameter. A chi-square distribution with df equal to a, commonly arises from the sum of squares of a independent N(0,1) random variables. The mean is equal to the df and the variance is equal to twice the df.


## power 
- The power of an experiment is defined for specific alternatives, e.g., |μ1 − μ2| = 100, rather than for the entire, complex alternative hypothesis. The power of an experiment for a given alternative hypothesis is the chance that we will get a statistically significant result (reject the null hypothesis) when that alternative is true for any one realization of the experiment. Power varies from α to 1.00 (or 100α% to 100%). The concept of power is related to Type 2 error, which is the error we make when we retain the null hypothesis when a particular alternative is true. Usually the rate of making Type 2 errors is symbolized by beta (β). Then power is 1-β or 100-100β%. Typically people agree that 80% power (β=20%) for some substantively important effect size (specific magnitude of a difference as opposed to the zero difference of the null hypothesis) is a minimal value for good power.



# aic bic
- the model which has lower AIC value than the other is better than the other in the sense that it is less complex but still a good fit for the data.


# ANOVA vs TTEST 
- However, if you have more than two groups, you shouldn't just use multiple t-tests as the error adds up (see familywise error) and thus you increase your chances of finding an effect when there really isn't one (i.e. a type 1 error). Therefore when you have more than two groups to compare e.g. in a drugs trial when you have a high dose, low does and a placebo group (so 3 groups), you use ANOVA to examine whether there any differences between the groups.\

# When to Use Chi-Square Test for Independence
-The test procedure described in this lesson is appropriate when the following conditions are met: The sampling method is simple random sampling. The variables under study are each categorical. If sample data are displayed in a contingency table, the expected frequency count for each cell of the table is at least 5.  
- goodness of fit

#lurking variable -- 潜在变量

# Margin of Error

- In a confidence interval, the range of values above and below the sample statistic is called the margin of error.

# simultanesou inference
- Ifwearedoingmanyt(orother)tests,saym>1wecan control overall false positive rate at α by testing each one at level α/m.

- Known as “simultaneous inference”: controlling overall false positive rate at α while performing many tests.

# The Tukey’s test 
- verifies our observation in the interaction plot and F-test. With a moderate or high alcohol intake (2 or 4 intakes), sadness is significant in increasing the memory time co realatinon between each level of feactors
 
 
# clustered data, longitudinal data and repeated measure
 
 - In clustered data, the dependent variable is measured once for each subject, but the subjects themselves are somehow grouped (student grouped into classes, for example).  There is no ordering to the subjects within the group, so their responses should be equally correlated.

In repeated measures data, the dependent variable is measured more than once for each subject.  Usually, there is some independent variable (often called a within-subject factor) that changes with each measurement.

And in longitudinal data, the dependent variable is measured at several time points for each subject, often over a relatively long period of time.
 
 
### svm
-先保证正确classfication情况下
-在保证两边同时最多margin
- C 越大 越correct但是不是很smooth了boundary
- Gamma越大variance 越小 考虑更近的点所以boundayr看起来更加curve和曲折


## AUC ROC 
- AUC represents degree or measure of separability. It tells how much model is capable of distinguishing between classes. Higher the AUC, better the model is at predicting 0s as 0s and 1s as 1s. By analogy, Higher the AUC, better the model is at distinguishing between patients with disease and no disease
- https://towardsdatascience.com/understanding-auc-roc-curve-68b2303cc9c5

## SVM SUPPORT VECTOR MACHINE
## svm

- Hopefully it’s becoming clearer what Sebastian meant when he said Naive Bayes is great for text--it’s faster and generally gives better performance than an SVM for this particular problem. Of course, there are plenty of other problems where an SVM might work better. Knowing which one to try when you’re tackling a problem for the first time is part of the art and science of machine learning. In addition to picking your algorithm, depending on which one you try, there are parameter tunes to worry about as well, and the possibility of overfitting (especially if you don’t have lots of training data).

- Our general suggestion is to try a few different algorithms for each problem. Tuning the parameters can be a lot of work, but just sit tight for now--toward the end of the class we will introduce you to GridCV, a great sklearn tool that can find an optimal parameter tune almost automatically.


## What is STATISTICAL SIGNIFICANCE?
● Statistical significance refers to the unlikelihood that mean differences observed in the sample have occurred due to sampling error. Given a large enough sample, despite seemingly insignificant population differences, one might still find statistical significance.
What is PRACTICAL SIGNIFICANCE?

● Practical significance looks at whether the difference is large enough to be of value in a practical sense.


## confidence limit 
-  If the confidence limits are small, researchers have a high degree of assurance that results are true or nearly true. Conversely, if the confidence limits are large, researchers must be more cautious.

##  Analysis 
is a detailed examination of something in order to understand its nature or determine its essential features. 

## Data analysis 
- is the process of compiling, processing, and analyzing data so that you can use it to make decisions.

## big data in business
- Effective data analysis solutions require both storage and the ability to analyze data in near real time, with low latency,
while yielding high-value returns.

## . The challenges
- identified in many data analysis solutions can be summarized by five key challenges: volume, velocity, variety, veracity, and value.

## logstical traing or not 
- I do not think you need to divide the set if you are interested in the significance of a coefficient and not in prediction. Cross validation is used to judge the prediction error outside the sample used to estimate the model. 

## text analytics
https://www.lexalytics.com/technology/sentiment-analysis

## the function of ‘Unsupervised Learning’?
> a) Find clusters of the data
> b) Find low-dimensional representations of the data
> c) Find interesting directions in data
> d) Interesting coordinates and correlations
> e) Find novel observations/ database cleaning
> 
> 

## What are the two paradigms of ensemble methods?
- The two paradigms of ensemble methods are
	- a) Sequential ensemble methods
	- b) Parallel ensemble methods


## Gini 
- Gini impurity[edit]
Used by the CART (classification and regression tree) algorithm for classification trees, Gini impurity is a measure of how often a randomly chosen element from the set would be incorrectly labeled if it was randomly labeled according to the distribution of labels in the subset. The Gini impurity can be computed by summing the probability 
- It reaches its minimum (zero) when all cases in the node fall into a single target category.


## balance data is important 
- SMOTE - Supersampling Rare Events in R

- 



## model seelction 
### PRESS statistic
- PRESSp an empirical measure of the prediction error of the model (called generalization error in machine learning).
• Can use PRESSp as a model selection criteria.

1. Leave one data-point out,
2. fit the model,
3. try to predict the deleted data-point.

- Using PRESSp is equivalent to leave-one-out cross-validation. (Also known as jack-knifing in this case.)

 


## Data mismatch is to deal with distribution mismatch



## Matthews correlation coefficient


Matthews correlation coefficient
From Wikipedia, the free encyclopedia
Jump to navigationJump to search
The Matthews correlation coefficient is used in machine learning as a measure of the quality of binary (two-class) classifications, introduced by biochemist Brian W. Matthews in 1975.[1] It takes into account true and false positives and negatives and is generally regarded as a balanced measure which can be used even if the classes are of very different sizes.[2] The MCC is in essence a correlation coefficient between the observed and predicted binary classifications; it returns a value between −1 and +1. A coefficient of +1 represents a perfect prediction, 0 no better than random prediction and −1 indicates total disagreement between prediction and observation. The statistic is also known as the phi coefficient. MCC is related to the chi-square statistic for a 2×2 contingency table

## Gain or lift curve
is a measure of the effectiveness of a classification model calculated as the ratio between the results obtained with and without the model. Gain and lift charts are visual aids for evaluating performance of classification models.


## PCA works for cv while Kmeans not because its unsupervized and does not have error

http://alexhwilliams.info/itsneuronalblog/2018/02/26/crossval/
such as clustering, there is usually no clear definition of error. Due to this, also cross-validation cannot be used for this purpose. 


## sensitivity 
- In medical diagnosis, test sensitivity is the ability of a test to correctly identify those with the disease (true positive rate), whereas test specificity is the ability of the test to correctly identify those without the disease (true negative rate).



## data science 
- hypoesis driven 
	- given the problem, we look for the fit data 
- data driven 
	- given the data, we try to come up with problems to solve 
		- that being said: we try to think what to learn from the data and what action to take
		
	
## types of data
- structured data : tables, spreadsheet, relational database 
- unstructured: non tables, images, audios, blobs of texts
- quantitative data: numerical height etc. 
- categorical data ； labelled and group data完全取决于 如何分类数据
- big data: cannot fit the volumes: growing volumes, cannot fit the memory of a single machine, 


## data sources:

- Most Common Data Formats CSV, XML, SQL, JSON, Protocol Bu↵ers
- Data Sources Companies/Proprietary Data, APIs, Gov- ernment, Academic, Web Scraping/Crawling

## two types of data science problems to solve: 

- Classification: Assigning something to a discrete set of possibilities. e.g. spam or non-spam, Democrat or Repub- lican, blood type (A, B, AB, O)
- Regression: **Predicting** a numerical value. e.g. some- one’s income, next year GDP, stock price





# Probability Overview: 

- Experienment: procedure that yields one of possible sets of outcomes 
- Dependence: intersection of AB if AB indepedent: PA*PB
- Conditional Probability: P(A|B) = P(A,B)/P(B)
- Bayes Theorem: P(A|B) = P(B|A)P(A)/P(B)
- Marginal Prob: **P(A)**  ??????? 


## Probability Distributions
- **Probability Density Function (PDF)** Gives the prob- ability that a rv takes on the value x: pX(x) = P(X = x) 
- **Cumulative Density Function (CDF**) Gives the prob- ability that a random variable is less than or equal to x: FX(x)=P(Xx)

Note: The PDF and the CDF of a given random variable contain exactly the same information.


## Descriptive Statistics

- Centrality:
	- Arithematic Mean:  best when character symmetric distribution without outliers: 1/n sigma X
	- Geometric Mean: Always smaller than arithematic means: useful to capture averaging ratios mean = Nth root of a1 a2 ...a3 N次根号下a1* a2* a3 ... an
	- median 
	- mode: most frequent value


- variabiliy:
	- **standard deviation**: Measure the *square differenc*e between the elements and mean 看每个直的平方和平均值差多少 **REMEMBER TO /(N-1) GIVEN LARGE N FOR DEGREE OF FREEDOM**
	- Variance V = SIGMA SQAURE 2

- variance interpret: Variance is an inherent part of the universe. It is impossi- ble 
to obtain the same results after repeated observations of the same event due to random noise/error. Variance can be explained away by attributing to sampling or measurement errors. Other times, the variance is due to the random fluctuations of the universe.


- Correlation Analysis: Correlation coefficients r(X,Y) is a statistic that measures the degree that Y is a function of X and vice versa. Correlation values range from -1 to 1, where 1 means fully correlated, -1 means negatively-correlated, and 0 means no correlation.


### Person Coeffcicent: 

- Measures the degree of the relationship between linear related variables: R

**Note: Correlation does not imply causation**

### Spearman Rank Coeffcient: 
- Computed on ranks and depicts **monotonic**  ????? relationship



# data clearning:

it is the process to turn data into **clean** and **analyzable**


## Errors vs. Artifacts
1. **Errors**: information that is lost during acquisi- tion and can never be recovered e.g. power outage, crashed servers

2. **Artifacts**: systematic problems that arise from the data cleaning process. these problems can be corrected but we must first discover them

##### DATA CLEARNING WOULD ALSO CAUSE PROBLEMS HERE CALLED ARTIFACTS


## Data Compatibility
 - Data compatibility problems arise when merging datasets
 	- units:
 	- numbers：
 	- names:
 	- time/date
 	- currency

## Data Imputation: 
- the process of dealing with missing data, and the methods depend on the type of data we deal with.
	- drop the records containing missing data 
	- **Heuristic-Based**: make a reasonable guess based on
knowledge of the underlying domain
	- Mean value fill
	- random value fill
	- Nearest Neighbor
	- **Interpolation**: use a method like linear regression to predict the value of missing data, thats what I have used for the kaggle competition


## Data outlier:
- usually arised from data collecting
- use sanity check to solve the problem



!!!!!!!!!
## Miscellaneous
**Lowercasin**g, removing non-alphanumeric, repairing, unidecode, removing unknown characters


### ALways use the raw data to clean, don;t start from a precleaned data. 
### always remember to reserve the raw data intact to keep the original accuracy
### Any type of data cleaning/analysis should be done on a copy of the raw data.



## Feature engineer: 
Feature engineering is the process of using domain knowl- edge to create features or input variables that help ma- chine learning algorithms perform better. 

- help increase the predictive power 
- FE is one of the most important steps in creating a good model


# different ways to deal with data:

## Continuous Data 
- Methods:
	- Raw Measures: data that hasn’t been transformed yet
	- Rounding: sometimes precision is noise; round to nearest integer, decimal etc.. **Round the data can kill the noise sometimes**
	- Scaling: Z log, maximax scale imputation 
	- binning the data: transform to groups for closed 
	- Interactions: interactions between features: e.g. sub- traction, addition, multiplication, statistical tes
	- statistical transformation: log/ **power** transform **Helped skewed distribution moe normal**

### BOX-COX
- AND
	- Row Statistics: number of NaN’s, 0’s, negative values, max, min, etc
	- **Dimensionality Reduction: using PCA, clustering, factor analysis etc**


FACTOR ANALYSIS
PCA
CLUSTERING: CROSS VALIDATION IS NOT WORKING FOR THIS beucase there is no specific errors 


## Discrete Data:

- method
	- Encoding: important to ML, sinece some of them DOESNT WORK FOR CATE DATA
	- ordinal: convert cate to orderd number: **WHY DO THIS**
	- **One-Hot Encoding: each of the m features becomes a vector of length m with containing only one 1 (e.g. [r, g, b] becomes [[1,0,0],[0,1,0],[0,0,1]])**
	- **Feature Hashing Schem**e: turns arbitrary features into indices in a vector or matrix
	- Embeddings: if using words, convert words to vectors (word embeddings)



## Statistical Analysis:
Process of statistical reasoning: there is an underlying population of possible things we can potentially observe and only a small subset of them are actually sampled (ide- ally at random).


Probability theroy gives prop- erties our sample should have given the properties of the population


but **statistical inference** allows us to deduce what the full population is like after analyzing the sample.

# probability 是通过population推测 sample的概率表现
# st infere 通过研究sample 推测整体





## Monte Carlo Sampling 
In higher dimensions, correctly sampling from a given distribution becomes more tricky. Generally want to use Monte Carlo methods, which typically follow these rules: define a domain of possible inputs, generate random inputs from a probability distribution over the domain, perform a deterministic calculation, and analyze the results.


## Inverse Transform Sampling 
Sampling points from a given probability distribution is sometimes necessary to run simulations or whether your data fits a particular distribution. The general technique is called inverse transform sampling or Smirnov transform. First draw a random number p between [0,1]. Compute value x such that the CDF equals p: FX(x) = p. Use x as the value to be the random value drawn from the distribution described by FX (x).






## Classic Statistical Distributions

Modeling- Overview
Modeling- Philosophies
### Binomial Distribution (Discrete)
Assume X is distributed Bin(n,p). X is the number of ”successes” that we will achieve in n independent trials, where each trial is either a success or failure and each success occurs with the same probability p and each failure occurs with probability q=1-p.


### Gausian 
```
Assume X in distributed 
Generalization
Bias Variance Trade-O↵ Inherent part of predictive modeling, where models with lower bias will have higher variance and vice versa. Goal is to achieve low bias and low variance.
of the binomial distribution as n ! 1.

```
### Poisson 

Assume X is distributed Pois Poisson expresses
the probability of a given number of events occurring
in a fixed interval of time/space if these events occur



## Prediction

We treat fˆ as a black box, since we only care about the accuracy of the predictions, not why or how it works.



## Inference
we want to understand the relationship between X and Y. We can no longer treat fˆ as a black box since we want to understand how Y changes with respect to X = (X1, X2, ...Xp)