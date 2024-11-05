# FraudFighter
Analyzing credit card data to predict fraudulent transactions. 

**Data Set Used**
This data set is comprised of synthetically created legitamate and fradulant transactions for 1,000 customers and 800 merchants. Data was created using Sparkov Data Generation Github tool (https://github.com/namebrandon/Sparkov_Data_Generation) created by Brandon Harris and compiled by Kartik Shenoy for download (https://www.kaggle.com/datasets/kartik2112/fraud-detection?resource=download).

Data colunms include transaction date time, cc number, merchant and category, ammount of transaction, name and gender and job of cardholder, street as well as longitute and laditude of cardholder billing information and merchant location. Finally, there is a binary fraud indicator.

**Intent and Process**
Using the procided data set, supervised machine learning tools will be used to predict if a credit card transaction is fradulent. 


1) Remodel the features for analysis
    - If the order is placed on weekday or weekend
    - Hour encoding for transaction time during work hours
    - Time since last transaction
    - Card use frequency in last 7 days
    - Card use frequency in last 30 days
2) One hot coding for gender, category and job
3) Random Forest with hypertuning
4) Assign a clustering value to each transaction and compare to the cluster value of the cardholder history. Bigger changes increases fraud chance
   - Cardholder clustering
   - merchant clustering with amount, category and location



Future work: 
- Import national holiday calendar to provide additional information if it is a workday, holiday, or weeked.
- Analyze fraud for different market time periods. (Ex: gift card fraud for certain merchants may increase around holiday season)
- Correlate buying time with type of merchant to predict fradulent if purchasing outside of typical buying time (Ex: groceries may be bought through workweek while eating at a fancy resteraunt most often occurs on Friday and Satudray evening).
