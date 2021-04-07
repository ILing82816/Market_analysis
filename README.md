# Marketing Analytics: Email Campaign Analysis
* Created a Email classifier that predicting whether a user opens the emails to help company marketing strategies.
* Used data set of Shopee Code League 2020 Data Science in Kaggle (https://www.kaggle.com/davydev/shopee-code-league-20/tasks?taskId=1574). 
* Optimized Logistic Regression, Naive Bayes, Random Forest, XGBoost, and LightGBM to find the best model.   

## Code and Resources Used
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, xgboost, lightgbm, hyperopt, matplotlib, seaborn, plotly   

## Data Collecting
In the dataset, we got the following features:
* User-specific information
* Email nature
* Users' engagement on the platform
* Users' reaction to the email, including whether users opened the email  

## Data Cleaning
I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:
* change the data type: date to integer.
* fill the missing variable by mean or mode.

## EDA
* Target variables: there are imbalance data  
![alt text](https://github.com/ILing82816/Market_analysis/blob/master/target.png "target")
* Feature Distribution  
![alt text](https://github.com/ILing82816/Market_analysis/blob/master/distribution.PNG "distribution")
* Category variable (country code)
![alt text](https://github.com/ILing82816/Market_analysis/blob/master/country_code.PNG "category")    

## Model Building  
I tried six different models and evaluated them using Matthews correlation coefficient (MMC).  
I tried six different models:  
* **Logistic Regression** - Baseline for the model
* **Logistic Regression with elatic net** - Add regularization term.
* **Naive Bayes** - linear model.
* **Random Forest** - Use more complexity non-linear model.
* **XGBoost, LightGBM** - Because of the ensemble model improving weak classifiers, I thought XGBoost and LightGBM would be effective.   

## Model performance
The LightGBM model have more good fit on the train and validation sets.
* **LightGBM:** MCC on validation sets = 0.53
![alt text](https://github.com/ILing82816/ds_disease_proj/blob/master/xgboost.png "XGBoost")  
 
