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
First, accuracy can give us a sense of how predictive the model is. 
Second, depending on the goal, we care about recall and precision.
Like in the disease setting, we more care about how many sick people we can identify rather than the overall accuracy. Because it's more important to find all sick people. In this case, recall is what we care most.
In general there's sill a tradeoff between recall and precision.
ROC curve is similar to precision recall curve. In roc we use false positive rate as y-axis and true positive rate as x-axis.
Auc is the area under the roc curve, the larger the auc the better.

