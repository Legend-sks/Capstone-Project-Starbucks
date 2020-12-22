# Capstone-Project-Starbucks
This is Capstone Project for Udacity Data Scientist Nano Degree Program. 

## Acknowledgements
Data for this project was provided by Udacity and Starbucks. I have used sevaral method leanrt during my Nano-degree course, I thank all my tutors from the learning videos for creating a well structured learning program.

## Project Overview
This Capstone Project is done as part of final delivarable to Udacities Data Scientist Nano Degree Program. Project choosen for this is the "Starbucks Project". This is a  classification problem which can help Starbucks to optimize app offers for their customers. it very crucial to identify right customers and send them just the write offer to maximize the customer value for company and at the same time provide the offer that best suits the customer. A customer will react to an offer based on various individual traits. Here I will analyze the dataset provided by Starbucks and try to answer few problems using model and visualization.

## Problem Statement:
I want to answer below three questions in this analysis:
1. Buying pattern of new app customers vs old app customers? Find the relationship, if any, between amount of purchases made by customers with the amount of time they have been a customer for Starbucks?
2. Demographic description of customers, 1. Who spend the most , 2. who like BOGO offers most, 3.Which of the four BOGO offers is more famous?
3. A machine learning model to predict which Offers sent to customers will be successfully completed.
  
 ## Dependencies or Libraries used
 
 Below libraries were used in this project.
1. pandas
2. numpy
3. datetime
4. seaborn
5. matplotlib.pyplot
6. from sklearn.model_selection import train_test_split
7. from sklearn.ensemble import RandomForestClassifier
8. from sklearn import preprocessing
9. from sklearn.preprocessing import StandardScaler, normalize, MinMaxScaler
10. from sklearn.metrics import confusion_matrix,accuracy_score, classification_report,f1_score
11. from sklearn.model_selection import GridSearchCV
12.from sklearn.preprocessing import StandardScaler
13.from sklearn import preprocessing
14.from sklearn.linear_model import LogisticRegression
15. from sklearn.ensemble import AdaBoostClassifier


## Evaluation Metrics
For model evaluaiton, I will be using f1-score metric to assess models performance. We will also measure accuracy of the model on test data to see how well our model predicts if the offer is successfull or not.

## Dataset Introduction
Starbucks has provided a simulated dataset that contains details about customer, offers and transactions. Each person in the simulation has some hidden traits that influence their purchasing patterns and are associated with their observable traits. People produce various events, including receiving offers, opening offers, and making purchases. There are three types of offers that can be sent: buy-one-get-one (BOGO), discount, and informational. In a BOGO offer, a user needs to spend a certain amount to get a reward equal to that threshold amount. In a discount, a user gains a reward equal to a fraction of the amount spent. In an informational offer, there is no reward, but neither is there a requisite amount that the user is expected to spend. Offers can be delivered via multiple channels. 

### Data Dictionary:

1. profile.json :Rewards program users (17000 users x 5 fields)
gender: (categorical) M, F, O, or null
age: (numeric) missing value encoded as 118
id: (string/hash)
became_member_on: (date) format YYYYMMDD
income: (numeric)

2. portfolio.json : Offers sent during 30-day test period (10 offers x 6 fields)
reward: (numeric) money awarded for the amount spent
channels: (list) web, email, mobile, social
difficulty: (numeric) money required to be spent to receive reward
duration: (numeric) time for offer to be open, in days
offer_type: (string) bogo, discount, informational
id: (string/hash)

3. transcript.json : Event log (306648 events x 4 fields)
person: (string/hash)
event: (string) offer received, offer viewed, transaction, offer completed
value: (dictionary) different values depending on event type
offer id: (string/hash) not associated with any "transaction"
amount: (numeric) money spent in "transaction"
reward: (numeric) money gained from "offer completed"
time: (numeric) hours after start of test

## Solution Summary

In this project I tried to answer three questions. Two of them were answered using data analysis and visualization and one using a machine learning model. At the start of the project the data set looked huge but at the end it proved to be a bit small. The model i created will benefit from more data around customer purchase behaviors and offer influence. Also we can use some more parameter/variables about the customer and the transactions.

I created 2 models, one using Logistics regression and one using Random forrest classificatoin and found that the Random forrest has better accuracy and F1 Score. Even after tuning Randon forrest was better model, I checked the robustness of my model using K-Fold cross validation.

Data cleaning part was a bit tricky as we have very less information to link the various events. Its sad that we I was not able to use the transaction data and understand the influence of informational offers.
There is some scope of improvement here, we can use a more sophisticated model like Adaboost or XGboost for this classification problem. I believe it will give  better accuracy and F1 scores. Also I have created a offer_view flag which I did not use in any analysis we can use this flag and try to link it with transactions event rows to get some idea on influence of informational offers.

More details about project finding can be read from the blogpost : https://shashik19.medium.com/udacity-capstone-project-starbucks-coffee-b136aa636bb6




























