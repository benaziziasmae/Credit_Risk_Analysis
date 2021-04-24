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

- Data source: 
- Software : Python 3.7.9, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3


## Results and summary 

1- RandomOverSample model

![balance_accurency_score](/Resources/balance_accurency_score.PNG)

![predict_score_high_low](/Resources/predict_score_high_low.PNG)

**Comments:**

- the balanced accuracy score is 66%
- The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 64%.

2- Smote model

![smote_model](/Resources/smote_model.PNG)


![smote_model2](/Resources/smote_model2.PNG)

**Comments:**
- The results are a bit different from the previous model.
- The balanced accuracy score is 51%.
- The high_risk precision is about 1% only with 59% sensitivity which makes a F1 of 1% only.
- Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 44%


3- ClusterCentroids model


![smoteen_model](/Resources/smoteen_model.PNG)



![smoteen_model2](/Resources/smoteen_model2.PNG)

**Comments:**

- Here the balanced accuracy score is down to about 52%.
- The high_risk precision is still 1% only with 63% sensitivity which makes a F1 of 1%.
- Due to the high number of false positives, the low_risk sensitivity is only 40%.

![ensemble_model](/Resources/ensemble_model.PNG)

![ensemble_model2](/Resources/ensemble_model2.PNG)

