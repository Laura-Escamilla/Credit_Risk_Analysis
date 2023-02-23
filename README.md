# Credit_Risk_Analysis

## Overview of the análisis

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, for this project we employed different techniques to train and evaluate models with unbalanced classes. We used  imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. 
Then, we used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 
Finally, we evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.


## Results

First, we used two Python libraries: imbalanced-learn and scikit-learn to evaluate three machine learning models by using resampling to determine which is better at predicting credit risk.

We created training and target variables by converting the string values into numerical ones using the get_dummies() method, create the target variables, and check the balance of the target variables.

<img width="402" alt="Split_the_data" src="https://user-images.githubusercontent.com/113747210/220795908-6e0da6cf-5a6c-4dcc-9221-cacd4338271b.png">

Next, we resample the training data. We used RandomOverSampler, SMOTE and ClusterCentroids algorithms to resample the data. For each resampling algorithm we did the following:
•	Use the LogisticRegression classifier to make predictions and evaluate the model’s performance.
•	Calculate the accuracy score of the model.
•	Generate a confusion matrix.
•	Print out the imbalanced classification report.
With RandomOverSampler model we got the following results:
-	The balance accuracy score is 65%
-	The high risk precision rate is 1% while recall is 72%
-	For the low risk we have a precision of 100% and recall of 59%
We can see our code and results in the image below:

<img width="437" alt="Random_Over_Sampler" src="https://user-images.githubusercontent.com/113747210/220796152-8c34ce59-87f2-4df9-9a12-20a2896907fc.png">

With SMOTE (Synthetic Minority Oversampling Technique) model we got the following results:
-	Here we can see a balanced accuracy score of 66%
-	The high risk precision rate is at 1%
-	The low risk precision rate is at 100% and recall at 69%
We can see our code and all the results in the next image:

<img width="438" alt="SMOTE" src="https://user-images.githubusercontent.com/113747210/220796196-884c09f2-244e-43b6-8df4-6798770e64ea.png">

Undersampling

With ClusterCentroids Model we got the following results:

-	We got a balanced accuracy score of 54%
-	A high risk precision rate of 1% and recall at 69%
-	The low risk precision rate is 100% while the recall is 40%

We can see the whole code and results in the next image:

<img width="439" alt="Cluster_Centroids" src="https://user-images.githubusercontent.com/113747210/220796254-44b0d36c-fa88-4dfc-a60d-906731e976af.png">

Combination sampling

We tested a combination over and under sampling algorithm, we resample the data using the SMOTHEEN algorithm. We got the following results:

-	We got a balanced accuracy score of 64%
-	A high risk precision rate of 1% and recall at 72%
-	The low risk precision rate is 100% while the recall is 57%

We can see the whole code and results in the next image:

![Combination](https://user-images.githubusercontent.com/113747210/220796308-28c4aa75-e192-41d2-b6eb-50f520ff0bff.png)

Balanced Random Forest Classifier

We used a Balanced Forest Classifier algorithm and got the following results:

-	We got a balanced accuracy score of 78%
-	A high risk precision rate of 3% and recall at 70%
-	The low risk precision rate is 100% while the recall is 87%

We can see the whole code and results in the next image:

![BalancedRandomForestClassifier](https://user-images.githubusercontent.com/113747210/220796704-2c7d52f7-eee4-4a1b-be9a-89dde9ea5190.png)

Easy  Ensemble AdaBoost Classifier

We used an Easy Ensemble AdaBoost Classifier algorithm and got the following results:

-	We got a balanced accuracy score of 93%
-	A high risk precision rate of 9% and recall at 92%
-	The low risk precision rate is 100% while the recall is 94%

We can see the whole code and results in the next image:

<img width="442" alt="image" src="https://user-images.githubusercontent.com/113747210/220796788-acc73d0e-14a3-4e86-bdc8-d018e4428f08.png">

## Summary

According to the accuracy rate we have the Easy Ensemble Classifier with a 93%, followed by the Balanced Radom Forest Classifier with 78%, then SMOTE with a 66%, Random Over Sampler got a 65%, SMOTEEN with 64.7% and the last one the Cluster Centroids with a 54% accuracy.

Therefore, after reviewing all models we can see that the Easy Ensemble Classifier got an accuracy rate of 93%, a high risk precision of 9%, the recall was at 92%, these are the higher results comparing all the models. For the “low risk” we got a 94% which means that this would be the recommendation to be used when performing a study like this. 









