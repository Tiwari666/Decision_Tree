# Why decision tree over the linear regression and logistic regression?
a) Handling Complex and Non-Linear Relationship: 
linear models are good when the data itself has a linear relationship.

Decision trees, on the other hand, are helpful since they can model more complex classification or regression problems with non-linear relationships in an explainable way.

b)  Handling outliers and missing values:
logistic regression is much affected by outliers and missing values  in the dataset. However, decision trees are able to handle missing values and outliers in the data much better then a logistic regression. A decision tree is not affected by outliers because it splits the data based on the feature values. Outliers are just considered as another data point with a specific feature value, and the tree will split the data accordingly. Even if an outlier falls into a leaf, the leaf will still have a mixture of examples from different classes. Therefore, the leaf will be impure, and the label will be determined by the majority class.

c) In additions, the logistic regression algorithm uses Maximum Likelihood Estimation (MLE) to estimate the parameters of the model, which is sensitive to outliers. MLE assumes that the data is normally distributed, but outliers can cause the distribution to deviate from normality, leading to biased estimates of the parameters.

d) Additionaly, Logistic regression is specifically designed for binary classification problems. However, the decision tree works even when the target variable has more than two classes.

e) Handling Large and High-Dimensional Data:
Decision trees can automatically select the most important features, reducing the dimensionality of the data. Logistic regression, on the other hand, uses all features at once, which can make it harder to interpret and understand the model when the number of features is high. Logistic regression tends to perform better with small sample sizes than decision trees. Decision trees require a large number of observations to create a stable and accurate model, and are more prone to overfitting with small sample sizes.


To sum up, the decision trees are a good choice when the relationship between the predictors and the response is complex and non-linear, when interpretability is important, when dealing with missing values or outliers, when handling large and high-dimensional data, and when the target variable has more than two classes.


# Decision Tree:
A decision tree is a supervised machine learning algorithm used for both classification and regression tasks. It creates a tree-like model of decisions based on features in the input data, where each internal node represents a feature, each branch represents a decision rule, and each leaf node represents an outcome or a predicted value.

There are 2 types of Decision trees: 

		Classification trees are used when the dataset needs to be split into classes that belong to the response variable. 

		Regression trees, on the other hand, are used when the response variable is continuous. 

 In other words, regression trees are used for prediction-type problems while classification trees are used for classification-type problems.


# How Classification and Regression Trees Work:

A classification tree splits the dataset based on the homogeneity of data. Say, for instance, there are two variables; salary and location; which determine whether or not a candidate will accept a job offer.

If the training data shows that 95% of people accept the job offer based on salary, the data gets split there and salary becomes a top node in the tree. This split makes the data “95% pure”. Measures of impurity like entropy are used to quantify the homogeneity of the data when it comes to classification trees.

In a regression tree, a regression model is fit to the target variable using each of the independent variables. The data is then split at several points for each independent variable.

At those points, the error between the predicted values and actual values is squared to get “A Sum of Squared Errors”(SSE). The point that has the lowest SSE is chosen as the split point. This process is continued recursively.

# Some terminologies in the Decision Tree:

Root node: The topmost node in a tree. Initial node of the decision tree: where the entire population or dataset starts dividing based on various features or conditions.

Leaf/ Terminal Node:  Nodes where further splitting is not possible, often indicating the final classification or outcome. Leaf nodes are also referred to as terminal nodes.

Splitting:  The process of dividing a node into multiple sub-nodes.

Parent and Child Node: A node, which is divided into sub-nodes is called the parent node of sub-nodes whereas sub-nodes are the child of the parent node.

Decision Node: Nodes resulting from the splitting of root nodes are known as decision nodes (also knowm as the internal node). These nodes represent intermediate decisions or conditions within the tree.

Internal node: Any nodes that lie in between the root node ( beginning node with the entire dataset) and the leaf nodes ( final decision nodes) are called decision nodes (also knowm as the internal node).

Branch: A subsection of the decision tree consisting of multiple nodes.


 # Gini index
The Gini index is a measure of impurity in a set of data. It is calculated by summing the squared probabilities of each class. A lower Gini index indicates a more pure set of data.
 # Information gain
Information gain is a measure of how much information is gained by splitting a set of data on a particular feature. It is calculated by comparing the entropy of the original set of data to the entropy of the two child sets. A higher information gain indicates that the feature is more effective at splitting the data.
# Impurity?
Impurity is a measure of how mixed up the classes are in a set of data. A more impure set of data will have a higher Gini index.

# When to use Gini index and information gain?
Gini index and information gain can be used interchangeably, but there are some cases where one may be preferred over the other. Gini index is typically preferred when the classes are balanced, while information gain is typically preferred when the classes are imbalanced.


![image](https://github.com/Tiwari666/Decision_Tree/assets/153152895/125efb3f-03c3-4c61-9427-7562169f870a)



# Steps to build the decision tree:

1.Choose the initial dataset with the feature and target attributes defined.

2.Calculate the Information gain and Entropy for each attribute.

![image](https://github.com/Tiwari666/Decision_Tree/assets/153152895/7db12b09-2fc0-42bf-a12a-361f811f95a3)


3.Pick the attribute with the highest information gain, and make it the decision root node.

4.Calculate the information gain for the remaining attributes.

5.Create recurring child nodes by starting splitting at the decision node (i.e for various values of the decision node, create separate child nodes).

Repeat this process until all the attributes are covered.

7.Prune the Tree to prevent overfitting.


![image](https://github.com/Tiwari666/Decision_Tree/assets/153152895/7ffa8e45-2b61-4bf4-95d2-3798734aa6b4)




Advantages of Decision Trees
1. Decision trees are easy to interpret.

2. To build a decision tree requires some data preparation from the user but normalization of data is not required.


Limitations/Disadvantages of Decision Trees
1. Decision trees are likely to over-fit noisy data. The probability of overfitting on noise increases as a tree gets deeper.


# What are the best ways to avoid overfitting in decision trees? 

# What is overfitting?
Overfitting is a common problem in machine learning, where a model learns the noise and irrelevant details of the training data, instead of the underlying patterns and relationships. This makes the model too complex and specific to the training data, and reduces its ability to adapt to new data. Overfitting can be detected by comparing the training and validation errors of the model. If the training error is much lower than the validation error, it means that the model is overfitting the training data.

# How to prevent overfitting?

There exists various techniques to prevent overfitting in decision trees, including pruning, regularization, and ensemble methods. Pruning involves removing  or merging branches or nodes that contribute minimally to the tree's accuracy or complexity, and it can be implemented before or after the tree reaches full growth, using criteria like information gain, error rate, or confidence interval. Regularization entails imposing constraints or penalties on tree growth, such as limiting depth, node count, or minimum samples for a split, to decrease complexity and variance while preventing overfitting. Ensemble methods combine multiple decision trees into a unified model, as seen in random forest or gradient boosting, which enhance accuracy and robustness by reducing bias and variance in individual trees and averaging out errors and noise.



#How to apply pruning?

Pruning is one of the most effective ways to avoid overfitting in decision trees, as it can reduce the size and complexity of the tree, and improve its generalization and interpretation. Pruning can be applied either before or after the tree is fully grown, using different methods and criteria. Pre-pruning, also known as early stopping, is the process of stopping the tree growth before it reaches its maximum depth or size, based on some threshold or condition. For example, you can stop the tree growth when the information gain or the error reduction of a split is below a certain value, or when the number of samples in a node is below a certain minimum. Post-pruning, also known as cost-complexity pruning, is the process of removing or collapsing branches or nodes after the tree is fully grown, based on some measure of complexity or error. For example, you can remove or collapse branches or nodes that have a high complexity or a low error reduction, or that have a low confidence interval or a high error rate.

# How to apply regularization?

Regularization is another way to avoid overfitting in decision trees, as it can limit the growth and complexity of the tree, and prevent it from becoming too specific or noisy. Regularization can be applied by imposing some constraints or penalties on the tree growth, such as the depth, the number of nodes, the number of leaves, the minimum samples required for a split, or the minimum samples required for a leaf. These parameters can be set manually or automatically, depending on the data and the objective. For example, you can set the maximum depth of the tree to avoid creating too many branches or levels, or you can set the minimum samples required for a split to avoid creating too many splits or nodes. Regularization can help reduce the variance and improve the simplicity of the tree, and avoid overfitting.

# How to apply ensemble methods?
Ensemble methods present an alternative approach to mitigate overfitting in decision trees via combining multiple trees into a singular model, thereby enhancing the model's accuracy and robustness. These methods can be implemented using various algorithms or techniques, including bagging, boosting, or stacking. 

Bagging, or bootstrap aggregating, involves generating multiple trees from diverse subsets of the training data and subsequently averaging or voting their predictions, thereby reducing variance and noise while bolstering model diversity and stability. 

Boosting, also referred to as gradient boosting, entails the sequential creation of multiple trees, with each subsequent tree aiming to rectify errors made by preceding trees and assigning weights to their predictions, thereby mitigating bias and error in individual trees and improving model accuracy and performance. 

Stacking involves the creation of multiple trees from distinct subsets or features of the training data, followed by the utilization of another model, such as logistic regression or a neural network, to combine their predictions, thus enhancing model flexibility, complexity, accuracy, and performance.






# Pruning to Reduce the Decision Tree: 
Decision trees are a popular machine learning tool that can be used for both classification and regression tasks. They areintuitive and easy to interpret, making them valuable in many domains. However, decision trees tend to grow excessively large
when given a large amount of training data, which can lead to overfitting.

Overfitting occurs when a model learns the training data too well, including all the noise and irrelevant patterns, and fails to generalize well to unseen data. This is where pruning comes into play.

Pruning is a technique used in decision tree algorithms to reduce the size of the tree by removing unnecessary branches. Thegoal of pruning is to simplify the decision tree while maintaining or even improving its predictive accuracy on unseen data.
Pruning helps to simplify the decision tree by removing branches that do not contribute significantly to its predictive accuracy.

By doing so, it reduces the risk of overfitting and improves the generalization ability of the decision tree.







Sources: 

Link 1: https://gustavwillig.medium.com/decision-tree-vs-logistic-regression-1a40c58307d0

Link 2: https://why-change.com/2021/11/13/how-to-create-decision-trees-for-business-rules-analysis/

Link 3:https://medium.com/analytics-vidhya/decision-trees-explained-in-simple-steps-39ee1a6b00a2

Link 4: https://www.linkedin.com/pulse/gini-index-information-gain-machine-learning-dhiraj-patra/

Link5: https://www.numpyninja.com/post/is-decision-tree-a-classification-or-regression-model

Link 5: https://www.linkedin.com/advice/0/what-best-ways-avoid-overfitting-decision-trees-skills-data-mining




