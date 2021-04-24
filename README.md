# Credit_Risk_Analysis

## Overview of the project 

The purpose of this analysis was to create a supervised machine learning model that could accurately predict credit risk. 
We use Python to build and evaluate several machine learning models to predict credit risk.
We adopted the following procedure:

- Oversample the data using the RandomOverSampler and SMOTE algorithms.
- Undersample the data using the ClusterCentroids algorithm.
- Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
- Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.


## Resources

- Data source: [LoansStat-2019](/LoanStats_2019Q1.csv)
- Software : Python, Anaconda Navigator, Jupyter Notebook


## Results and summary 

**1- Naive Random Oversampling**

![balance_accurency_score](/Resources/balance_accurency_score.PNG)

**Confusion Matrix**

![predict_score_high_low](/Resources/predict_score_high_low.PNG)

**Comments:**

- Accuracy Score: 66%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 66%
- Recall Low Risk: 67%

**2- SMOTE Oversampling**

![smote_model](/Resources/smote_model.PNG)

**Confusion Matrix**

![smote_model2](/Resources/smote_model2.PNG)

**Comments:**
- Accuracy Score: 51%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 62%
- Recall Low Risk: 64%

**3- Undersampling model**

![undersampling](/Resources/undersampling.PNG)

**Confusion Matrix**

![undersampling2](/Resources/undersampling2.PNG)

**Comments:**
- Accuracy Score: 51%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 59%
- Recall Low Risk: 43%


**4- Smoteen model**


![smoteen_model](/Resources/smoteen_model.PNG)

**Confusion Matrix**

![smoteen_model2](/Resources/smoteen_model2.PNG)

**Comments:**

- Accuracy Score: 61%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 70%
- Recall Low Risk: 54%


**5- Balanced Random Forest Classifying**

![balance_random_forest](/Resources/balance_random_forest.PNG)

**Confusion Matrix**

![balance_random_forest2](/Resources/balance_random_forest2.PNG)

- Accuracy Score: 78%
- Precision High Risk: 4%
- Precision Low Risk: 100%
- Recall High Risk: 67%
- Recall Low Risk: 91%



**6- Easy Ensemble Classifying**

![ensemble_model](/Resources/ensemble_model.PNG)

**Confusion Matrix**

![ensemble_model2](/Resources/ensemble_model2.PNG)

- Accuracy Score: 92%
- Precision High Risk: 7%
- Precision Low Risk: 100%
- Recall High Risk: 91%
- Recall Low Risk: 94%


## Summary 

This analysis is trying to find the best model that can detect if a loan is high risk or not. Becasue of that, we need to find a model that lets the least amount of high risk loans pass through undetected. That correlating statistic for this is the recall rate for high risk. Looking through the different models, the ones that scored the highest were:

- Easy Ensemble Classifying (91%)
- SMOTEENN Sampling (70%)


While this is the most important statistic that is pulled from this analysis, another important statistic is recall rate for low risk as it shows how many low risk loans are flagged as high risk. Looking through the different models, the ones that scored the highest were:

- Balanced Random Forest Classifying (91%)
- Easy Ensemble Classifying (94%)

After taking these two statistics over the others, we can look at the accurary score to get a picture of how well the model performs in general. The models with the highest accuracy scores were:

- Easy Ensemble Classify (94%)
- Balanced Random Forest Classifying (92%)

After factoring in these three main statistics, the model that I would recommend to use for predicting high risk loans is the Easy Ensemble Classifying model.
