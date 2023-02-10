# Bank Customer Churn Prediction
![bank-teller-6330466_960_720](https://user-images.githubusercontent.com/113230957/218202121-fa8442c9-8d16-4611-a3fb-2cbf8fe71972.png)

<hr>
## Overview

Churn rate is the measure of how many items or individuals are moving out of a particular group, in this case how many customers are unsubscribing from a bank's services.Customer churn has become a major problem among for many businessed given that their revenue stream is directly related to the amount of customers that subscribe and pay for their services and products therefore earning them revenue. 
<hr>
## Business and Data Understanding

It is important for a business to be able to identify customers at risk of churning and come up with startegies that will maximize the likelihood of the customer staying.This is quite difficult especially for a large banking institution with many different types of customers, to know why a customer is cancelling their subscription to its services because of their different behaviours and preferences.In the current digital environment where it is very easy for a customer to switch from one banking institution to another , customer churn prediction will allow a bank to identify when a customer is about to leave and act proactively to reverse a potential customer chrun and mitigate revenue losses.

This project will use a dataset obtained from 
<a href = 'https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset'> Bank Customer Churn Dataset </a>
.The dataset represents customers of ABC Multinational Bank which is a European bank operational in 3 countries namely France, Germany and Spain. It has 10,000 observations and 12 features.
<hr>
### A Few Findings From EDA
<br>
The bank's customers comprise of more Males than Females.
There are also more female churned customers than there are male, showing that the likelihood of a female customer unsubscribing from the bank's services

<br>

![churn_gender](https://user-images.githubusercontent.com/113230957/218202307-fd4a2f54-ee16-4b06-a378-63d37961e2b8.PNG)

<br>
<hr>
Germany has the highest number of churned customers, followed closely by France with Spain having the smallest number.

![country churn](https://user-images.githubusercontent.com/113230957/218202425-2a426bca-e03f-4648-a12b-70a10f71894f.PNG)

<br>

<hr>
Distribution of Churn among the numerical features

<br>
![churn vs various variables](https://user-images.githubusercontent.com/113230957/218202536-a56828db-e914-49d1-892d-5e7c7c40df27.PNG)


<br>

## Modeling
3 models were used for classification:

<hr>
1. Logistic regression - with a few transformations done to the data.

<br>
![logreg](https://user-images.githubusercontent.com/113230957/218202636-0ccb680e-8280-4201-bf5c-348af9c2ba4a.PNG)

<hr>
2. Random Forest Classifier
A random forest model that uses a pipeline to pass transformers and GridSearchCv to find the the best hyperparameters for the model.

<br>
![rf](https://user-images.githubusercontent.com/113230957/218202748-0021e57e-e073-46fe-b0df-768633167bc1.PNG)

<br>
<hr>
3. XGB Boost Classifier
A more complex model that is fitted to the data after feature engineering and more transformations are done to the data to maximize model performance.

<br>
![xgb](https://user-images.githubusercontent.com/113230957/218202783-aaba6f44-b76e-4898-b2b6-e2ffb765d692.PNG)

<br>
<hr>
## Evaluation

Various evaluation metrics were employed but f1 score was the most significant as there was a class imbalance propblem.
Overall the XGB classifier performed the best.

<br>
![model performances](https://user-images.githubusercontent.com/113230957/218202814-fb625112-c968-4799-8898-2bd52d3d28ca.PNG)

<hr>
<br>
![rf cm](https://user-images.githubusercontent.com/113230957/218202833-5c3965b1-fe6f-4add-b901-695c30104886.PNG)

<hr>
<br>
![lr_cm](https://user-images.githubusercontent.com/113230957/218202857-59626aeb-8888-4e4c-a638-5dd32369200b.PNG)

<hr>
<br>
![xgb cm](https://user-images.githubusercontent.com/113230957/218203047-0ebbccb6-ecd8-4d7c-b8a0-5572176742ac.PNG)

<hr>

## Conclusion
<hr>
1. The best performing model was the XGB boost which had the highest accuracy score and tied with the Random Forest calssifier on the f1 score.

2. All three models were able to predict the unchurned class well but failed to achieve good scores inpredicting the Unchurned class
<hr>
