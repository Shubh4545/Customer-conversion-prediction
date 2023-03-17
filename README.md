# Customer-conversion-prediction

Welcome to the Customer-conversion-prediction- wiki!
## Project Goal
The goal of the Customer Conversion Prediction project is to build a machine learning model that can predict whether a client will subscribe to the insurance based on their demographic and marketing data. The project aims to help the insurance company identify the customers that are most likely to convert, so that they can be targeted via call and the cost of telephonic marketing campaigns can be reduced. The historical sales data provided will be used to train and evaluate the performance of the machine learning models. The analysis of the model will be done to identify the important factors that contribute towards the conversion and the AUROC metric will be used to evaluate the model's performance. The main objective of the project is to develop an accurate and efficient model that can aid the insurance company in improving its sales conversion rate and reducing marketing costs.

#

## Project Aproach:
For this project, I utilized Google Colab as my integrated development environment (IDE) for programming in Python. Google Colab is a robust tool provided by Google that is well-suited for implementing machine learning algorithms, performing data analytics and cleaning operations, and developing data science models.

## Project Implementation Steps:

## 1.Libraries Import and Load Dataset
We have imported requrired libraries and also loaded [dataset](https://github.com/Shubh4545/Customer-conversion-prediction/blob/53c1bda14fe9d7de665f6d17ec3976c9d6e4fa31/dataset.csv)

## 2.Clean Dataset
we have used functions like remove duplicates,dropped null values,missing values,check data type and removal of outlires.

## 3.Exploritory Data Analysis
For the good model fit and accuret prediction we've explore the data and done Univariate Analysis, Bivariate Analysis, Correlation Check. Data type check and take dummies.

### 3.1 Univariate Analysis
![y](https://github.com/Shubh4545/Customer-conversion-prediction/blob/eacbe608c8ec7e3a3a12abe3dedf50b2ec96642e/Resources/DependentFeature.png)
#### The class distribution in the target variable is ~89:11 indicating an imbalance dataset

![age](https://github.com/Shubh4545/Customer-conversion-prediction/blob/15ec09e1efda7cb94f556fc9fa0b68817a1ea4bc/Resources/Age_Univariate.png)
#### Age 

### 3.2 Bivariate Analysis

We've check and learn that which type of occupations have more chances to subscribe our term insurance policy.
![job-VS-Y](https://github.com/Shubh4545/Customer-conversion-prediction/blob/15ec09e1efda7cb94f556fc9fa0b68817a1ea4bc/Resources/job%20vs%20Purchased.png)

### 3.3 Correlation 
We've checked correlation between differant variables. We can see here Duration of Call is Highly correlated to our target variable.

![Corelation](https://github.com/Shubh4545/Customer-conversion-prediction/blob/15ec09e1efda7cb94f556fc9fa0b68817a1ea4bc/Resources/corr.png)

## 4.Encoding
we have used Label and one hot encodeing for this features['job', 'marital', 'education_qual', 'call_type', 'mon', 'prev_outcome']

## 5.Split Dataset
SMOTE Oversampling we are using due to imbalence data

0    39477

1    29496

## 6.Scalling
We used StandardScaler

## 7.Models
### We used Linear regression,xgboost and Random Forest 
 ![Models](https://github.com/Shubh4545/Customer-conversion-prediction/blob/15ec09e1efda7cb94f556fc9fa0b68817a1ea4bc/Resources/RESUL%20TABLE.png)
### we can see that Dur(Duration) is most important feature in dataset
 ![feature importance](https://github.com/Shubh4545/Customer-conversion-prediction/blob/2eb11e9a622e9ab8c6e0bd4e4511d26f04472c4b/Resources/feature%20importnace.png)

## 7.Model Evaluation
### We are going to comapre auroc curve 
![model Evaluaton](https://github.com/Shubh4545/Customer-conversion-prediction/blob/269361de6c388e3960ddb08f55e79542d93ad7c0/Resources/auroc%20curve.png)

# Conclusion
Based on the results obtained from the evaluation of the three classification models (Logistic Regression, XGBoost, and Decision Tree Classifier) on the given historical data, XGBoost outperformed the other models with the highest accuracy score of 93.54% and the highest AUROC score of 0.986.

This implies that XGBoost is a suitable model for predicting whether a client will subscribe to the insurance or not. It is recommended to deploy this model in the production environment to accurately target potential customers and optimize marketing costs.

However, further analysis is recommended to identify the important features contributing to the model's performance and to fine-tune the model for better results.


## Further Scope
The current project has successfully built and evaluated a machine learning model to predict whether a customer will subscribe to an insurance policy. However, there is still room for improvement and further scope in this project, which includes:

Feature Engineering: The current dataset includes limited features, and feature engineering could be performed to extract more relevant features from the given data or other external sources, which could enhance the model's performance.

Hyperparameter Tuning: Hyperparameter tuning of the model could be performed to optimize its performance further. By varying the hyperparameters of the model and evaluating its performance, we could achieve better results.

Deployment: The current model could be deployed in a production environment, integrated with the company's systems, and used to target potential customers effectively.

Exploratory Data Analysis (EDA): Exploratory data analysis could be performed on the data to gain insights into the customers' behavior, which could help in understanding the customers' preferences, demographics, and other characteristics that influence their decision-making.

Model Comparison: In addition to the models evaluated in this project, other classification models could also be implemented and compared to identify the best performing model for this problem.

Regular Maintenance: As the company's customer base grows and changes, the model's performance might degrade. Regular monitoring and maintenance of the model are necessary to ensure it continues to perform effectively.

Overall, these enhancements and improvements could help the insurance company to optimize its outreach efforts and improve the success rate of selling insurance policies to potential customers.
