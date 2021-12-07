# Credit_Risk_Analysis
## Purpose
This machine learning project used scikit-learn and imbalanced-learn to train and evaluate models to determine credit card risk using a credit card credit dataset.
Six different techniques were used to train and evaluate models to determine credit risk: Oversampling with the RandomOverSampler and SMOTE algorithms, Undersampling with the ClusterCentroids algorithm, a combination of over and under sampling with the SMOTEENN algorithm, and two machine learning models that reduce bias - the BalancedRandomForestClassifer and EasyEnsembleClassifier.
## Results
### Naive Random Oversampling
![naive_random_sampling](https://user-images.githubusercontent.com/87148177/144769749-df6dd046-df9c-4cff-85a9-a2c8036e6575.png)\
-The balanced accuracy score was 0.6496, meaning the model predicted the credit risk accurately 64.96% of the time.\
-The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.\
-The recall scores for this model show that the model is better at identifying positive low-risk loans (0.68) and decent at positively identifying high-risk loans (0.62)
### SMOTE Oversampling
![SMOTE](https://user-images.githubusercontent.com/87148177/144769913-f4a515bd-d462-49c2-affc-f6d5e64386db.png)\
-The balanced accuracy score was 0.6444, meaning the model predicted the credit risk accurately 64.44% of the time.\
-The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.\
-The recall scores for this model show that the model is better at identifying positive low-risk loans (0.66) and decent at positively identifying high-risk loans (0.63)
### Undersampling
![undersampling](https://user-images.githubusercontent.com/87148177/144769992-4c2da386-0d37-4e58-8dd5-2b02bf20f987.png)\
-The balanced accuracy score was 0.5292, meaning the model predicted the credit risk accurately 52.92% of the time.\
-The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.\
-The recall scores for the high-risk loans were around 0.61 and the recall scores for low-risk loans were around 0.45. While the high-risk recall is much better, both recall scores are low and show that many of the positives were not accurately predicted.
### Combination (Over and Under) Sampling (SMOTEENN)
![combination_sampling](https://user-images.githubusercontent.com/87148177/144770064-242e683b-a185-4a0d-90be-d4a32db7be51.png)\
-The balanced accuracy score for the undersampling technique was around .6245, meaning that only 62.45% of the testing data was accurately classified.\
-The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted.\
-The high-risk recall score for this model is fairly high at 0.68 and the low-risk recall score is average at 0.57. Compared to the previous techniques, this model is much better at identifying true high-risk loans.
### Balanced Random Forest Classifier
![random_forest](https://user-images.githubusercontent.com/87148177/144770218-f2f7b1fd-21b8-41bc-9eb4-a5a89be862c5.png)\
-The balanced accuracy score for this model is comparatively high at .7878, meaning that 78.78% of the testing credit data was accurately classified.\
-The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted.\
-The recall score for low-risk loans is very high at 0.91 and the recall score for high-risk loans is fairly high at 0.67. This shows that the classifier is good at predicting true positives for low-risk loans.
### Easy Ensemble AdaBoost Classifier
![easy_ensemble](https://user-images.githubusercontent.com/87148177/145123349-ad76c3a4-a190-406b-9b8a-bfa07a9acb5e.png)\
-The balanced accuracy score for this model was 0.9254, meaning the model was accurate 92.54% of the time.\
-The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted.\
-The recall score was high for both low and high risk loans: 0.91 for high risk and 0.94 for low risk.
## Summary
All of the machine learning models had low precision scores for the high-risk loans in accurately predicting positives. The balanced accuracy score for the models I completed varied with the lowest score for the undersampling method and a high score with Easy Ensemble Classifier. Recall scores also varied between models with the lowest scores for undersampling and highest with the classifying methods. Of the models created, the Easy Ensemble Classifier would be the best model to use to predict credit risk due to the high recall scores for both high and low risk loans, as well as an accuracy score of 92.54%. The precision for this model is still very off, indicating that the positives are not necessarily accurate, and so this model could be much improved before being put into use.
