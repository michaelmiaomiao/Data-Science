2018(1-3月) 分析|数据科学类 博士 全职@Facebook - 猎头 - 其他  | Pass | 在职跳槽
之前发的how to cracking the data challenge得到大家好评，很多战友们发来站内信询问如何准备面试。于是再接再厉，把自己的经验总结出来，造福更多的战友们！

先说一下自己的情况，我自己是转专业的，没有相关的学位，国内学校普通，国外更是3流大学读的研究生，年纪还比较大，资质普通的不能再普通的普通人。但是我比较善于总结，比较有耐心（其实就是挂的太多了）。说这些就是希望鼓励那些转专业没有啥信心的同学们，我这么不利的情况下都可以做到，相信只要你不放弃，有策略的去准备，最后一定能有个好结果的。

这次我主要想总结一下如何准备Data Science analytics interview，重点会放在大家都头疼的case interview上面。

其实思路跟我写的那篇如何准备data challenge差不多，首先你要先明确目标。data science有很多track：analytics, inference, machine learning。很多同学在面试初期犯的错误就是：只要是个ds职位就去面，但是并没有考虑到自身的情况，你适合什么职位，有多少时间准备。每个人精力有限，这里的每个方向准备的东西都不太一样，都准备的很细真心没那么多时间。那么大家会说了：我没啥工作经验，也不知道自己适合什么职位。这个时候可以在面试初期多试试不同的职位，如果你面了3家类似的职位，感觉问题很难，一面就挂了，说明你自己准备不够，或者这个职位不适合你。我在面试初期也犯了这种错误，面了很多ml职位，还有混到on site的，结果都是被一通虐。我自己还是准备了一些ml的东西。发现很多基础的东西都不懂，问的深入了就不行了。后来主攻analytics方向，基本所有的都能到on site阶段了，这个时候就离拿到offer不远了。我想说的就是，找准一个方向准备，往最深最细的方向去准备。这里给大家科普一下data science的整个life cycle，airbnb的这篇文章介绍的很好：https://medium.com/airbnb-engineering/at-airbnb-data-science-belongs-everywhere-917250c6beba

假设你的目标就是analytics方向，你要准备的顺序或者花的时间应该是这样：sql/r/python+case study > experiment design > machine learning。所以重点就是sql+case study。我下面就把这三个主题应该如何准备给大家说一下，重点还是放在case study上面

SQL/PYTHON/R: 这里主要就是考察data munipulation，你能不能把复杂的逻辑转换到代码执行上面。

SQL:sql我暂时没有看到特别好的资料，觉得最有用的还是地里的面经。如果真的一点都不懂的话，可以看看w3 school上面的题目，再把leetcode上面database的题目练习一下就行。最后面试前还是得刷面经，重点是逻辑一定要清楚,边缘case考虑到。我遇到的sql常考的有：各种join, union/except/intersect, 各种aggregate function（sum, ncount, average), case when, windows function（lag, lead, rank)。把我说的这几个都懂明白了怎么用，应该应付一般的sql没啥问题。不过sql很多时候都是逻辑比较复杂，真正写起来并不复杂，这种只能靠多见题目了，没有啥捷径
Python/R: 我主要用python，考的题目无外乎就是把sql题目再用python写一遍，基本都是用pandas来写。如果对pandas不太熟悉，可以看看kaggle上面别人用python写的代码，主要看他们如何做data munipulation那块。另外对基本的数据结构也要了解，比如什么是list, tuple, set, dictionary。各大网站都有很多python的公开课，有时间就自己去上上吧，毕竟打好基础挺重要的。实在没时间就把kaggle别人写的代码弄明白了就够用了

Case study: 重中之重！这块有点像咨询公司的case interview，也是考察能不能把问题break down，能不能发散把各种情况想的比较全面。不同的是，我们ds面case interview，更关注从数据的角度去解决问题，从用户使用产品的life cycle出发去定义metrics。但是我还是建议去看一下咨询公司面试题目，学习一下他们答题的stucture，如何跟面试官保持一个很愉快 conversation。这里推荐Victor Cheng的case study interview, 可以从喜马拉雅fm里面听，很适合上下班的时候听：http://www.ximalaya.com/5269453/album/6414597?feed=reset。 下面我来总结一下典型的case study常见题目以及答题思路。这类问题并没有一个统一的答案，只要是合理的就可以。

Diagnostic problem: 这类问题通常是发现某个kpi某天突然下降了，该咋办？这类问题就是考察你能不能把一个business问题一步一步的break down，找到问题所在。一般的思路都是先从数据搜集的是否正确，是否这个kpi有seasonality，这个kpi有哪些不同的segment，等等这几点出发。举个最简单的例子：某社交网络发现用户使用likes的功能今天突然下降了10%，你觉得是为啥？首先你可以问面试官，咱们的数据搜集的正确与否，这个功能是不是有seasonality, 是不是今天有个speicial events发生（比如自然灾害，大家都断网了）。切记要keep this as a conversation，不要你一个劲儿的在那里说说说。根据面试官给你的引导，下一步就是如何break down, 你可以先说，likes下降了是指哪个部分下降了，有friends post, pages, or events。你还可以从另外一个角度break down，比如是哪个地区的likes下降了。记住，understand the context is very important!。不要先急着答题，要先把数据的背景了解清楚。基本你把背景了解清楚了，也就找到了问题所在了。
How to measure the success of a new product/feature: 这类问题一般就是我想改变或者增加一个产品的功能，如何衡量是不是成功了。这种问题的思路一般都是先搞清楚产品的目标是什么，你可以问面试官：what is the goal of this product? 从目标出发，先定义衡量的metrics，然后就是做实验了，根据实验结果来判断是否成功。在定义metrics的时候要想的全，哪些metrics对你的目标是最重要的，另外也不要忘了定义counter metrics，我在下面会用一个例子来解释。定义metrics注意一点就是不要仍给面试官一堆list，想3个最重要的就可以了。做完实验后面试官会有一些follow up问题，比如metric a 增加，metric b减少；或者metric a增加了2%，那么这些情况下是否应该launch这个产品呢。我下面用一个例子来说明这类问题的思路。还是以社交网络为例子，他们改变friends recommendation 算法，希望用户可以通过这个功能多加好友，如何衡量这个feature是不是成功呢。我们先明确这个功能的目标，是希望多加好友，加了好友以后，希望在平台上有更多的交涉。那么这个时候的metrics可以应用funnel的思路来定义：好友增加率（friends request/accept rate)，月活量（monthly active user)，参与度(engagement），这些方面来定义metrics，尽量想到至少3个。然后做ab test，比较两个group的差别。这个时候面试官就会有一些follow up的问题，比如我们发现monthly active user(mau)增加了5%， 但是engagement 减少了3%，那么这个产品是好是坏呢。这个时候engagement就是我们的counter metrics，因为我们不仅希望加了好友以后，每个人的connection增加了，我们更看重是不是有意义的connection, 所以engagement也是一个很重要的指标。一般这种题目可以从短期vs长期效应来考虑。比如我们的mau增加了，虽然短期的engagement减少了，但是长期看的话，由于每个人的connection增加了，由于network effect，大家相互影响，engagement长期看也许会增加的，这个时候就要去衡量long term effect了。然后面试官可能会接着问，假设我们的metrics都正向增加了，比如2%，那么如何判定这个2% 是个好的增长，可以launch to everyone? 这个时候可以往量化方面想，比如2%的增加对应了多少popualtion，这个2%的增加带来的潜在revenue是多少，如果是好几百万的话，那即便2%，也是个很好的提升！
How to identify opportunity: 这类问题一般都是在做ab test之前，我如何去说服别人我的假设是合理的，我的假设值得去做一些test来衡量impact。这种问题很重要的一点就是identify opportunity sizing。也就是你的假设会影响多少人，如果只影响到5%的人，可能你带来的影响不会很大，但是如果超过20%的话，这个时候你的影响就大了。比如某电商想加个产品线，这个时候你如何去说服你的领导这个产品线值得去做一些实验呢。首先你要告诉你的领导，我加了这个产品线以后，会影响多少人，会带来潜在的多少收入。接下来就是如何去做这个产品线，比如我们应该target目标群是啥，应该以什么样的方式让目标群更好的了解我们的新产品线。再接下来就是如何做实验了，这样就回到了上面的how to measure the success的问题。从这里大家也可以看出，data science其实是一环套一环，有一个完整的周期的，我推荐的那篇airbnb的blog也说明了这一点。

实验设计：我自己的统计基础比较弱，这里就不班门弄斧了，就简单给大家说一说常见问题以及准备资料。

准备资料：在前一篇帖子里提到过：AB testing by Google from Udacity
常见问题：如何randommize sample, 如何决定sample size, 决定sample size的几个因素对sample size如何影响，如何决定test跑多久，什么是p value, confidence interval, type 1, type 2 error， 熟悉t test, z test公式跟原理。要注意不能只把定义背下来，要真正理解了，并且可以给non technical的人解释清楚。可以参考penn stats的假设检验章节：https://onlinecourses.science.psu.edu/stat414/node/290

Machine learning: analytics职位对ml要求很低，很多公司基本不问，问的话也都是基于你简历里面提到的模型，比如你提到random forest, 面试就会问你为啥选这个模型，如何评价模型好坏，这个模型的优缺点是啥这种非常标准化的问题，如果是classification problem，他们会问如何决定false positive or false negative重要。其实这个时候还是要结合产品来说。比如某信用卡fraud detection产品，那么减小false posititive就比较重要，因为如果你的false positive rate太高了，很多不应该被decline的人都被decline了，大家就不会用你的产品了。反之如果是癌症detection模型，那么false negtive就比较重要了，因为本来人家得了绝症，但是你没有发现，结果延误了治疗。这个知乎帖子总结了ml常见问题，对于面analytics，甚至inference track来说，都足够了。链接在这里：https://www.zhihu.com/question/62482926/answer/210531386?from=timeline&isappinstalled=0


最后对于转专业的同学来说，如果有时间精力跟金钱，还是可以考虑读一个data science相关的master program。湾区的同学推荐Master in Data Science from University of San Francisco。这个项目只有一年，强度很大，但是期间负责安排实习工作，毕业的人都能找到不错的工作，就算一开始是个不知名小公司，但是一年后都纷纷跳到了大公司。对于Ph.D的同学，可以考虑去个boot camp，首推insights data science，这个bar很高，但是只要进去了，工作都找的非常好，很多公司比如facebook ,airbnb等都跟他们有合作项目的，很多都是直接on site。

吐血总结了这么多，就是希望能够帮助更多的同学，尤其是转行的同学找到理想的工作。虽然ds这行比较杂，涉及多学科，不好准备。但是其实都是有套路可循的。还是多总结，多跟别人讨论。希望我的这点总结能够对大家有点指导意义。

- https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=455639&highlight=%BB%E3%D7%DC


- https://www.sisense.com/blog/5-steps-to-data-driven-business-decisions/



- What is AARRR?
AARRR stands for Acquisition, Activation, Retention, Referral and Revenue and is pretty much the bee’s knees when it comes to understanding your customers, their journey and optimizing your funnel as well as setting some valuable and actionable metric goals for your startup. It’s important to view the acquisition part holistically.
That means not just looking at site visitors but also at how many and how those site visitors convert to customers. Y

- https://medium.com/@ms.mbalke/aarrr-framework-metrics-that-let-your-startup-sound-like-a-pirate-ship-e91d4082994b

SaaS

- https://stellarpeers.com/blog/metrics-airbnb-experiences-feature/


## pm
- https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=206209

##
Graph and Network Analysis
Bayesian Statistics
A|B Testing
Supervised Learning
Linear Regression, SVM, Random Forest, Logistic Regression , KNN, etc...
Unsupervised Learning
K-Means Clustering, PCA, etc…
NLP, Model Validation, K-Folds, etc...
You should also have an understanding of basic concepts
Bias-Variance Trade-Off
Gradient Descent
**L1 / L2 Regularization**
Bagging / Boosting


## Algorithms and Data Structures
Distributed Computed (Spark)


