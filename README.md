# ML Model for Customer Churn Prediction for telecom companies
In the telecommunication industry, customers tend to change operators if not provided with attractive schemes and offers. It is very important for any telecom operator to prevent the present customers from churning to other operators.

Our objective would be to build an ML model which can predict if the customer will churn or not in a particular month based on the past data.

![chhurn.png](https://github.com/MallikaBera/mallikabera.github.io/blob/main/chhurn.png)

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
<!-- You can include any other section that is pertinent to your problem -->

## General Information
Customers usually do not decide to switch to another competitor instantly, but rather over a
period of time (this is especially applicable to high-value customers). In churn prediction, we
assume that there are three phases of customer lifecycle :

1. <u>The ‘good’ phase:</u> In this phase, the customer is happy with the service and behaves as usual.

2. <u>The ‘action’ phase:</u> The customer experience starts to sore in this phase, for e.g. he/she gets a compelling offer from a competitor, faces unjust charges, becomes unhappy with service quality etc. In this phase, the customer usually shows different behaviour than the ‘good’ months. It is crucial to identify high-churn-risk customers in this phase, since some corrective actions can be taken at this point (such as matching the competitor’s offer/improving the service quality etc.)

3. <u>The ‘churn’ phase:</u> In this phase, the customer is said to have churned. In this case, since you are working over a four-month window, the first two months are the ‘good’ phase, the third month is the ‘action’ phase, while the fourth month (September) is the ‘churn’ phase.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
**Model Selection**:  Since we have observed a clear imbalance of classes in the dataset, high training and test score alone can not help us to correctly identify True Positives. In order to identify the most suitable model, we have created and evaluated the performance of several classification models.  

The performance check for our tested models are : 

|<span style="color:Blue">Model</span> |<span style="color:Blue">Train Score</span>|<span style="color:Blue">Test Score</span>|<span style="color:Blue">AUC_ROC</span>| 
|:-----|:----:|----:|----:|
|Logistic Regression with RFE |0.91 |0.91 |0.91 |
|Logistic Regression with PCA |0.82 |0.82 |0.83 |
|Logistic Regression with PCA & Gridsearch|0.83 |0.83 |0.83 |
|Logistic Regression with DecisionTreeClassifier|0.93 |0.89 |0.83 |
|Logistic Regression with RandomForestClassifier|0.91 |0.91 |0.70 |
|Logistic Regression with XGBoostClassifier|0.91 |0.91 |0.70 |
|Decision Tree with GridSearch |0.83 |0.83 |0.83 |
|Decision Tree with PCA |0.83 |0.83 |0.72 |
|Random Forest with PCA |1.0 |0.91 |0.70 |
|XGBoost with PCA |0.90 |0.37 |0.72 |
      
Considering the Train Score, Test Score and AUC, we can recommend <span style="color:Yellow">**logistic Regression with RFE**</span> as the most effective model for the given dataset.

**Recommendations for telecom companies based on data analysis:**:            

- During the first two months, the chances of a customer to stop the service is almost same as happy customers but he chances decrease significantly in the action phase. If a customer does not churn in the first two months, he is more likely to continue the service in the next months. So telecom companies should try to make sure customers do not leave within the first two months(good phase)

- After the first two months, churn probability is higher for customers whose total recharge amount is low. So telecom companies can reach out to the customers who have started to recharge with lesser amount suddenly after few months of joining the network.

- It is seen that customers who recharges less number of times are more probable to churn, so telecom companies can revisit the customers who do not seem to increase their recharge count for a longer period of time.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Python - version 3.11.9
- Numpy - version 1.26.4
- Pandas - version 2.1.4
- Matplotlib - version 3.7.3
- seaborn - version 0.12.2
- sklearn - version 1.2.2
- statsmodels - version 0.14.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact
Created by [@MallikaBera] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project --># BikeSharingModel
