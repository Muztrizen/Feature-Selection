# Feature-Selection

## 1. Definition of Feature Selection
- Selecting a subset of the input features for training the model, and ignoring the irrelevant or redundant ones. 
- i.e., Simply dropping features if the features have large number of missing values.

## 2. Why need FS?
- To prevent overfitting.
- To reduce the number of predictors used to train a ML model. 
- To reduce calculation time (fewer predictors, less time needed to compute),
- To reduce training time, by reducing the number of features.
- To make ML model to be simple and explainable.
- To improve the interpretability of the model (easier to study the dependency of predictors when the number is smaller).
- To improve the accuracy of the predictive performance (by reducing the number of redundant predictors).
- To avoid poor quality model, by excluding non-informative features.

## 3. Method
1. Filter: Pearson Correlation, Chi-Squared

1. Wrapper:LASSO, Elastic Net, Ridge Regression

1. Embedded: 
  1. Forward Selection: The procedure starts with an empty set of features [reduced set]. The best of the original features is determined and added to the reduced set. At each subsequent iteration, the best of the remaining original attributes is added to the set.
  1. Backward Elimination: The procedure starts with the full set of attributes. At each step, it removes the worst attribute remaining in the set.
  1.Combination of forward selection and backward elimination: The stepwise forward selection and backward elimination methods can be combined so that, at each step, the procedure selects the best attribute and removes the worst from among the remaining attributes.
  1.Recursive Feature elimination: Recursive feature elimination performs a greedy search to find the best performing feature subset. It iteratively creates models and determines the best or the worst performing feature at each iteration. It constructs the subsequent models with the left features until all the features are explored. It then ranks the features based on the order of their elimination. In the worst case, if a dataset contains N number of features RFE will do a greedy search for 2N combinations of features.

Note: wrapper and embedded methods are normally “fine-tuned” to optimize the classifier performance, making them ideal if the goal is to objectively find out an ideal set of predictors for a specific learning algorithm or model.

## Reference:
https://towardsdatascience.com/the-5-feature-selection-algorithms-every-data-scientist-need-to-know-3a6b566efd2?gi=b724c65b5151
https://towardsdatascience.com/feature-selection-for-machine-learning-in-python-wrapper-methods-2b5e27d2db31
https://github.com/krishnadulal/Feature-Selection-in-Machine-Learning-using-Python-All-Code
https://towardsdatascience.com/the-5-feature-selection-algorithms-every-data-scientist-need-to-know-3a6b566efd2
