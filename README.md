# comparing_classifiers

### Understanding Data
The data is related to the direct marketing campaigns of a Portuguese bank, the marketing campaign is based on phone calls to assess if the bank deposit was subscribed or not.

The features in the dataset give various kinds of information regarding the callers' personal information like age, job, marital status, education, etc, other sections of the feature provide information about campaign type of contact, month, day, and some other campaign related information, and the last section of features describes the social and economic context.

### Business objective
The business objective is to develop a model that can clarify the factors contributing to the success of a customer subscribing to a deposit. This model is crucial for enhancing the efficiency of marketing campaigns. By pinpointing the key characteristics influencing success, it enables more effective management of resources, including human effort, phone calls, and time. Additionally, it facilitates the selection of a cost-effective and high-quality group of potential customers likely to make a purchase.

### Modeling
After splitting the data set to train and test the data set, a baseline model is created, the accuracy of this model is 0.88. This is a baseline model whatever the model created open should have better accuracy than this baseline model.

In the first iteration basic models for Logistic Regression, K-nearest neighbor (KNN), Decision Tree, and Singular Value Decomposition(SVM). In the second iteration, feature engineering, and hyperparameter tuning to simply the complexity of the performance and improve the accuracy.

### Conclusion
After the first iteration, the model comparison results show the logistic regression and SVM models perform better. Logistic regression which yields a high score, and minimal degradation in train score, with less fit time. Whereas, SVM shows almost the same score but has a high fit time compared to any other model.

The results of the first model take into consideration, that when the number of features increases the complexity increases, so it is important to reduce the unwanted features to improve the fit time. One of the approaches is, applying the ordinal encoding method for some features where there is a clear hierarchical, such as day_of_week, month, and education. Which reduces the number of features compared to the first iteration where hot encoding is used. The other approach is Recursive feature elimination and correlation matrix to help identify the least important features and remove them. Finally, find the best hyperparameters using a grid search to tune the model.

Fire iteration model comparison

![Screen Shot 2023-12-10 at 12 17 13 AM](https://github.com/vnyreddy/comparing_classifiers/assets/18583217/4aa437a1-0da1-4a76-aa96-67f75adc4183)

Second Iteration model comparison

![Screen Shot 2023-12-10 at 12 18 17 AM](https://github.com/vnyreddy/comparing_classifiers/assets/18583217/a8f769ff-8e0c-46c6-b688-125995d35506)

### Recommendation
After some feature engineering, reduction, and hyperparameter tuning, the training time is reduced significantly in KNN and Decision Tree models, and slightly better for logistic regression. Whereas, SVM training time is significantly increased.

Finally, after the second iteration Logistic regression and Decision Tree models are performing significantly well, similarly, KNN's performance is close to the other two models. Out of these three models, the Decision Tree is the best model for this problem as it has high accuracy and less training time.
