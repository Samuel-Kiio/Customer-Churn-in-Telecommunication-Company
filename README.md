Gg# Customer-Churn-in-Telecommunication-Company

![display_photo](https://github.com/Samuel-Kiio/Customer-Churn-in-Telecommunication-Company/blob/main/display_photo.png)

## Project overview

This project seeks to build a classifier to predict whether a customer will soon stop doing business with SyriaTel, which is a telecommunications company. It seeks to identify any predictable patterns among customers who have already left and use these features to predict customers who are likely to leave in the future. 

Customer churn is the loss of clients or customers. Predicting churn helps the Telecom company to:

1. Identify at risk customers and implement *highly targeted* efforts to stop them churning.
2. Identify pain points and friction across a customers journey.
3. Identify strategies that target these pain points to lower churn and increase retention rates.

## Business and Data understanding

### Business problem

SyriaTel, a telecommunication company is facing the problem of an increase in the number of customers who leave the company. A consistently high churn rate could result in the company quickly becoming unsustainable. 

Attracting new customers as a strategy is not enough to sustain the company for very long. 

It is therefore important for the company to increase the number of loyal and devoted customers by identifying the pain points across a company journey and accurately predicting the customers who are likely to churn and therefore targeting them using aggressive strategies to reduce these points of friction.

### Objectives

The main objective for this project is to build a prediction model that can accurately predict customers who are likely to churn from the company.
This objective will be achieved through the methods outlined in the specific objectives:

1. To build a machine learning model that can accurately predict customers  who will churn based on the features in the dataset.
2. To rank features these features in the dataset according to their order of significance

### Success criteria

The model performances will be compared using the Recall (Sensitivity) score. This is given by: (TP/TP+FN). 

From this, the aim is to reduce the number of false negatives, as it would be detremental for the model to predict that customers will are not going to churn while they actually will. 

A model with a recall of greater than 0.75 would be considered to be a successful model.

### The Data

The dataset used is from SyriaTel Telecommunication company. Each row represents a customer, and the columns contain customer’s attributes which are described in the following:
- state: the state the user lives in
- account length: the number of days the user has this account
- area code: the code of the area the user lives in
- phone number: the phone number of the user
- international plan: true if the user has the international plan, otherwise false
- voice mail plan: true if the user has the voice mail plan, otherwise false
- number vmail messages: the number of voice mail messages the user has sent
- total day minutes: total number of minutes the user has been in calls during the day
- total day calls: total number of calls the user has done during the day
- total day charge: total amount of money the user was charged by the Telecom company for calls during the day
- total eve minutes: total number of minutes the user has been in calls during the evening
- total eve calls: total number of calls the user has done during the evening
- total eve charge: total amount of money the user was charged by the Telecom company for calls during the evening
- total night minutes: total number of minutes the user has been in calls during the night
- total night calls: total number of calls the user has done during the night
- total night charge: total amount of money the user was charged by the Telecom company for calls during the night
- total intl minutes: total number of minutes the user has been in international calls.
- total intl calls: total number of international calls the user has done
- total intl charge: total amount of money the user was charged by the Telecom company for international calls
- customer service calls: number of customer service calls the user has done.
- churn: true if the user terminated the contract, otherwise false.

### The Target Variable

The target variable is "churn". This project seeks to compare the effects of the different variables in respect to the 'churn'. In order to visualize the churn rate in the organization, a plot was created

![target_variable](https://github.com/Samuel-Kiio/Customer-Churn-in-Telecommunication-Company/blob/main/target_variable.png)

## Modeling

The project is a binary classifier task. To solve this problem, the models that will be tried are:
1. Logistic regression
2. K-Nearest Neighbours
3. Decision Trees
4. Random Forest
5. Support Vector Machine

_Logistic regression is used to create the base model_

## Model evaluation

#### 1.) A machine learning model that can accurately predict customers  who will churn based on the features in the dataset.

![model_evaluation](https://github.com/Samuel-Kiio/Customer-Churn-in-Telecommunication-Company/blob/main/model_evaluation.png)

- The recall score was chosen as the ideal  evaluation metric. 

- This is because the goal of this project was to maximize the number of predictions of customers who are likely to churn. This means minimizing the number of false negatives, i.e the number of customers that the model predicts will not churn but they actually churn. 

- The problem is less sensitive to false positives at the expense of false negatives. This is because the problem suggests that the model would rather predict that a customer will churn and they fail to churn than predict that a customer will not churn and they actually end up churning. The latter would be more detrimental to the company financially than the former and thus the choice to select Redcall score as the ideal comparison metric.

#### 2.) A rank of features in the dataset according to their order of significance

![feature_ranking](https://github.com/Samuel-Kiio/Customer-Churn-in-Telecommunication-Company/blob/main/feature_ranking.png)

From the chart shown above, the top 5 most important features in the model prediction are:
1. Total Day minutes
2. Total Evening minutes
3. Number of customer service calls
4. The area code they live in. 
5. The total nighrt minutes. 

This shows that the customers who make spend the most amout of time in calls and also make the highest number of customer service calls are most likely to churn.

It also shows that it is not the people who make many calls, but those who spend more time on calls who are likely to churn

## Conclusion and recommendations

The objective of the project was to identify clients who are likely to churn, in order to deploy strategies that reduce the pain points of customers and increase retention. 
The data was drawn from the CyriaTel Telecommuication company. This data was ananlysed and cleaned. Class imbalance was found in the target variable. This was addressed by the use of the SMOTE technique in the test set.

Different classification models were tried out including Logistic regression, KNN, Decision tree, Random Forest and Support Vector Machine. 
The Decision tree model offered the best model. 

In conclusion,
1. The model that meets the the success criteria, in predicting customers who will churn, of a sensitivity/ Recall score of 0.75 is the Tuned decision tree model.
2. The most important feature in predicting the churn rate is the number of minutes a customer spends on a call coupled with the number of customer service calls.

## Next steps

The next steps in this project would be to investigate how the area code ranks so highly in feature importance and how it affects customer churn. This could be due to:
1. An area experiencing unstable network connection issues due to poor coverage.
2. A lagrer population in certain areas that could cause system overload on existing infrustructure.
3. Demographic issues in a certain area which are being addressed by a competing telecom company.