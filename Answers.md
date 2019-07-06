### PREDICTIVE MODELING
1
First identify if the response variable is a continuous one or discrete one, then to decide it's a 
regression problem or classification problem.
For regression, we can use linear model, regularized linear model, knn, random forests.
For classification, we can use logistic regression, knn, lda/qda, random forests, boosting, svm

2
You probably will not get the results that you want. The model ususally does not work. It might be low accuracy. It's dangerous to draw a conclusion without knowing that the distibution has changed. It's like you gathered US president election data, then you decided to use it to predict Russian president election. It's called covariate shift. 

3
For example, decision tree is a high variance model, hence it's sensitive to outlierss, we then can use  ensemble learning such as random forests to reduce variance, hence more robust to outliers.
Or for linear regression, we can use regularized linear regression to reduce variance.
In svm, you can control hyperparameter C to adjust the sensitivity of the model.
C -> very large, it is equal to hard svm
C -> small, underfitting, less sensitive 
The hard margin svm is prune to overfitting.

In general, this phenomeon is called bias-variance tradeoff. Decreasing variance will cause to increasing bias.

4
Absolute erorr is like finding the median, while square error is like finding the mean. When the data has significant outliers, it will affect square error a lot. However, absolute error usually will not be affected that much. 
$$|y - \hat{y}|$$ is less sensitive to outliers, while $$|y - \hat{y}|^2$$ is more sensitive to ourliers. In linear regression setting, lasso penalizes $$|w|$$, while ridge penalizes $$|w|^2$$. Lasso will give us sparse sollution, while ridge will not. 

5
 - First, accuracy can give us a sense of how predictive the model is. 
	Second, depending on the goal, we care about recall and precision.
	Like in the disease setting, we more care about how many sick people we can identify rather than the overall accuracy. Because it's more important to find all sick people. In this case, recall is what we care most.
	In general there's sill a tradeoff between recall and precision.
	ROC curve is similar to precision recall curve. In roc curve we use false positive rate as y-axis and true positive rate as x-axis.
	Auc is the area under the roc curve. The larger the auc, the better.
	f1-score: the weighted average of recall and precision
	support: how many evidence support that group
 - We can use undersamle or oversample. Or increase the size of dataset. For example, logistic regressio ususally needs large dataset size.
 - We can have recall and precision for each group.

 6
 Both SVM and Logistic Regression are discriminative models. SVM tries to maximize the margin, and Logistic Regression tries to maximize the maximal likelihood. Logistic Regression requires large data size. The fundamental difference is just the loss function.
 Naive Bayes uses Bayes' rule to predict. It is easy and fast and perfoms well in multi class prediction. However, it has assumptions like independent of predictorsm. If a category is not observed, we will have "Zero Frequency" problem, but we can use laplace smoothing.

 7

 8

 9
 Time series data. RNN model.

 10
 

### PROGRAMMING
1
use python's `itertool`, and then use `combinations` 

2
double for loop, and need another list to store count. Then can use `lst.index(e)` to get index for element `e` from list `lst`


### PROBABILITY


9
$$\frac{12!}{4!4!4!}$$

### STATISTICAL INFERENCE


### DATA ANALYSIS

2
In linear Model
$$R^2$$ is corrleration coefficients, $$\frac{1-RSS}{TSS}$$
The better one would be adjusted $$R^22$$, or other metrics such as AIC, BIC, Mallow's CP

3
It means p > n

4
Ideally yes, but it would be more cost-expensive to collect the data and compute the model.

### PRODUCT METRICS

### COMMUNICATION

