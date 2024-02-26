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

# Some twerminologies in the Decision Tree:

Root node: The topmost node in a tree.

Leaf/ Terminal Node: Nodes do not split is called Leaf or Terminal node.

Splitting: It is a process of dividing a node into two or more sub-nodes.

Parent and Child Node: A node, which is divided into sub-nodes is called the parent node of sub-nodes whereas sub-nodes are the child of the parent node.

Decision Node: When a sub-node splits into further sub-nodes, then it is called a decision node.


![image](https://github.com/Tiwari666/Decision_Tree/assets/153152895/125efb3f-03c3-4c61-9427-7562169f870a)



# Steps to build the decision tree:

1.Choose the initial dataset with the feature and target attributes defined.

2.Calculate the Information gain and Entropy for each attribute.

3.Pick the attribute with the highest information gain, and make it the decision root node.

4.Calculate the information gain for the remaining attributes.

5.Create recurring child nodes by starting splitting at the decision node (i.e for various values of the decision node, create separate child nodes).

Repeat this process until all the attributes are covered.

7.Prune the Tree to prevent overfitting.


![image](https://github.com/Tiwari666/Decision_Tree/assets/153152895/7ffa8e45-2b61-4bf4-95d2-3798734aa6b4)
















Sources: 

Link 1: https://gustavwillig.medium.com/decision-tree-vs-logistic-regression-1a40c58307d0

Link 2: https://why-change.com/2021/11/13/how-to-create-decision-trees-for-business-rules-analysis/

Link 3:https://medium.com/analytics-vidhya/decision-trees-explained-in-simple-steps-39ee1a6b00a2


