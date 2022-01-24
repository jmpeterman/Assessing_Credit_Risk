# Credit_Risk_Analysis

We are looking for a solution or process that can help us better understand how to assess credit risk for retail borrowers. We would like our solution to be accurate, scalable and efficient. There are many factors at play when assessing credit risk of retail borrowers. Below is a preliminary list to illustrate some of the variables that must be considered.

Challenges of assessing risk:

•	fragmented financial data

•	strength of risk model

•	lenth of process

•	overall envirnment

•	regulatory requirements

•	position in economic and credit cycle

•	difficulty predicting future cash flow of customer


# Overview of the loan prediction risk analysis:
For our project we are fucosing on one of these issues: model strength. We are going to try a number of different machine learning methods on historical data to see if any of them can provide a workable solution that is accurate, scalable and efficient.

Our data is provided by LendingClub. It is historical data from 2019. Using this recent data with the methods listed below we hope to find at least one method that can help our team better assess risk quickly and accurately.


List of models that we will test:

•	Oversampling

•	Undersampling
  
•	Combination Sampling
  
•	Ensemble methods

# Results:

How to understand the Imbalanced Classification Report:
We will see seven different metrics provided by our imbalanced classification report. Please review this section for a refresher on how to interpret these findings

PRE - Precision: Precision is the measure of how reliable a positive classification is. TruePositive / (TruePositive + FalsePositive)

REC - Recall: Recall is the ability of the classifier to find all the positive samples. TruePositive / (TruePositive + FalseNegative)

SPE - Specificity: the true negative rate. TrueNegative / (FalsePositive + TrueNegative). For imbalanced learning specificity is often more important. 

F1 - Combines precision and recall in an effort to balance both concerns. (2 * Precision * Recall) / (Precision + Recall)

GEO - Geometric Mean: GEO combines sensitivity and specificity into one score. sqrt(Sensitivity * Specificity)

IBA - Indexed Balance Accuracy: the balanced accuracy in binary and multiclass classification problems to deal with imbalanced datasets. It is defined as the average of recall obtained on each class. The best value is 1 and the worst value is 0 when adjusted=False. This is a relatively new metric. More information can be found here: https://link.springer.com/chapter/10.1007/978-3-642-02172-5_57#:~:text=This%20paper%20introduces%20a%20new,the%20highest%20individual%20accuracy%20rate.

SUP - Support: Support is the number of actual occurrences of the class in the specified dataset.

Method 1: Naive Randon Oversampling

![naive 1](https://user-images.githubusercontent.com/58608736/150695378-6d1b87ff-db34-45af-bce4-aa34c08138a1.PNG)
![naive 2](https://user-images.githubusercontent.com/58608736/150695389-6eaae0fe-1607-4832-8461-075e67ea8b26.PNG)


Method 2: SMOTE Oversampling

![smote 1](https://user-images.githubusercontent.com/58608736/150695408-670b290b-e19e-4086-951b-68e470927b43.PNG)
![smote 2](https://user-images.githubusercontent.com/58608736/150695412-a5110f60-64d5-4c09-bf42-043b90f85432.PNG)


Method 3: Cluster Centroids algorithm - Undersampling

![centroid 1](https://user-images.githubusercontent.com/58608736/150695444-6ef4046c-7e51-44d7-9478-f2025b205762.PNG)
![centroid 2](https://user-images.githubusercontent.com/58608736/150695447-78af7fed-4aa2-46ad-ba4a-d169cdf5f82d.PNG)


Method 4: SMOTEEN - Over/Undersampling

![combo smoteen 1](https://user-images.githubusercontent.com/58608736/150695475-c930f435-6f5e-4b59-974d-9cba4f87de4b.PNG)
![combo smoteenn 2](https://user-images.githubusercontent.com/58608736/150695482-d7319805-7060-49a6-9c7d-2ba4079c9d4c.PNG)


Method 5: Balaned Random Forest Classifier

![ensemble brf 1](https://user-images.githubusercontent.com/58608736/150695763-16b3e0b1-6d91-4ff7-82f4-4d8d1165e991.PNG)
![ensemble brf 2](https://user-images.githubusercontent.com/58608736/150695773-4e48b151-af14-417f-b180-a2bf792b3982.PNG)


Method 6: Easy Ensemble AdaBoost Classifier

![adaboost 1](https://user-images.githubusercontent.com/58608736/150695815-193b69e5-3973-4cc1-9870-c878cc43df7d.PNG)
![adaboost 2](https://user-images.githubusercontent.com/58608736/150695822-4f313271-dcc1-4e3f-8827-8989a8bc6ca9.PNG)


# Summary
After reviewing your accuracy scores and the extended classifier report for each method, we can clearly see that the Easy Ensemble AdaBoost Classifier is the method that we will move forward with. It returned a balanced accuracy score of 93.5% and the classification report reinforces our decision with its robust supporting classifier details.
