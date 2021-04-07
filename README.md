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
![alt text](https://github.com/ILing82816/Market_analysis/blob/master/target.png "distribution")
* Category variable (country code)
![alt text](https://github.com/ILing82816/ds_disease_proj/blob/master/var_corr.png "correlation")    

## Model Building  
I tried six different models and evaluated them using ROC curve. I chose ROC curve because it is relatively easy to interpret and check overfitting for this type of model.  
I tried six different models:  
* **Logistic Regression, KNN, Naive Bayes** - Baseline for the model
* **XGBoost, LightGBM** - Because of the ensemble model improving weak classifiers, I thought XGBoost and LightGBM would be effective.
* **Random Forest** - Because of larger variance of XGBoost and LightGBM, I thought random forest would be hlpful when the previous model easy to overfit.   

## Model performance
The Random Forest model have more good fit on the train and validation sets.
* **Random Forest:** Accuracy on train sets = 81%, Accuracy on validation sets = 80%
![alt text](https://github.com/ILing82816/ds_disease_proj/blob/master/random.png "random")  
* **Logistic Regression:** Accuracy on train and validation sets = 78%
* **KNN:** Accuracy on train sets = 75%, Accuracy on validation sets = 72%
* **Naive Bayes:** Accuracy on train sets = 82%, Accuracy on validation sets = 78%
![alt text](https://github.com/ILing82816/ds_disease_proj/blob/master/Naive%20Bayes.png "Naive")   
* **XGBoost:** Accuracy on train sets = 82%, Accuracy on validation sets = 80%
![alt text](https://github.com/ILing82816/ds_disease_proj/blob/master/xgboost.png "XGBoost")  
* **LightGBM:** Accuracy on train sets = 83%, Accuracy on validation sets = 80%
![alt text](https://github.com/ILing82816/ds_disease_proj/blob/master/lightgbm.png "LightGBM")  
