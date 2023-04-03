# Project_2-Customer-Churn-Prediction. Classification Problem
Data from https://www.kaggle.com/datasets/avhikj/churn-predictions-personal

A common issue for businesses across many industries is customer churn. If you want to grow as a company, you have to invest in acquiring new clients. Every time a customer leaves, a sizable investment is lost. Both time and effort need to be channeled into replacing them. Being able to predict when a client is likely to leave and offer them incentives to stay, can offer huge savings to a business.
Understanding what keeps customers engaged is therefore very important information because it can help you create retention strategies and implement operational procedures meant to prevent customers from leaving.

The project's objectives are to analyze the data, offer clarifications, and create a powerful predictive model. The accuracy of the model is critical to the success of any proactive retention efforts. That is why, for this project, I chose the recall metric. Reducing the number of false negatives is crucial.



#### <b> Objectives</b>
The following questions were answered:
* What's the % of Churn Customers and customers that keep in with the active services?
* Is there any patterns in Churn Customers based on the gender?
* Is there any patterns/preference in Churn Customers based on the type of service provided?
* What's the most profitable service types?
* Which features and services are most profitable?
* Many more questions that will arise during the analysis


Steps of project:
* EDA
* Data Preprocessing
* Building baseline models with unbalanced data
  ** Fandom Forest Classifier
  ** XGB Classifier
  ** LGBM Classifier
  ** CatBoost Classifier
* Building baseline models with balanced data 
  ** Fandom Forest Classifier
  ** XGB Classifier
  ** LGBM Classifier
  ** CatBoost Classifier
* Optuna optimization
  ** XGB
  ** LGBM
* SHAP Explainer
* Feature Importance
* Feature Selection
  ** XGB Classifier with selected features
  ** LGBM Classifier with selected features
* Lime with XGB Classifier
* Conclusion
* Addition. Customer Segmentation. Examine Kmeans Clustering vs Spectral Clustering vs Agglomerative Clustering. Built new XGB model based on customer segmentation.

 
 The final prediction consists of 0 and 1. 0 means the person is not exited and 1 means the person is exited.
 
 <b> Best XGB Classifier has following scores: </b>


<ul class="b">
  <li>train accuracy-score: 0.8168571428571428</li>
  <li>test accuracy-score: 0.8083333333333333</li>
  <li>roc_auc score:  0.7992637422337378</li>
  <li>pr_auc score:  0.6737417483518006</li>
  <li>Precision: 0.520</li>
  <li>Recall: 0.784</li>
  <li>F1 Score: 0.625</li>
</ul>

<table>
  <tr>
    <th>...</th>
    <th>precision</th>
    <th>recall</th>
    <th>f1-score</th>
    <th>support</th>
  </tr>
  <tr>
    <th>0</th>
    <th>0.94</th>
    <th>0.81</th>
    <th>0.87</th>
    <th>2389</th>
  </tr>
  <tr>
    <th>1</th>
    <th>0.52</th>
    <th>0.78</th>
    <th>0.62</th>
    <th>611</th>
  </tr>
  <tr>
    <th>accuracy</th>
    <th></th>
    <th></th>
    <th>0.81</th>
    <th>3000</th>
  </tr>
  <tr>
    <th>macro_avg</th>
    <th>0.73</th>
    <th>0.8</th>
    <th>0.75</th>
    <th>3000</th>
  </tr>
  <tr>
    <th>weighted avg</th>
    <th>0.85</th>
    <th>0.81</th>
    <th>0.82</th>
    <th>3000</th>
  </tr>
</table>

<p> However, in as much as the model has a high Recall, it still misses those who end up churning. This could be improved by providing retraining the model with more data over time. It is also important to impove Precision score, because right now model works as random for False Positives.</p>

<p> Addition. I added Customer Segmentation to improve XGB model. I made clustering by Balance, Credit Score and Estimated Salary to get a better understanding of them which in turn could be used to increase the revenue of the company. </p>

<h1> Conclusion </h1>
<p> Customer churn is definitely bad to a firm ’s profitability. Various strategies can be implemented to eliminate customer churn. The best way to avoid customer churn is for a company to truly know its customers. This includes identifying customers who are at risk of churning and working to improve their satisfaction. Improving customer service is, of course, at the top of the priority for tackling this issue. Building customer loyalty through relevant experiences and specialized service is another strategy to reduce customer churn. Some firms survey customers who have already churned to understand their reasons for leaving in order to adopt a proactive approach to avoiding future customer churn.</p>


