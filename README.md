# Background:
Churn is a key driver of EBITDA margin and an industry-wide challenge. A churned customer provides less revenue or zero revenue and icnreases competitor market share. It costs up to 5 times as much for an service provider to acquire a new subscriber as to retian an exising one. 
With the help of data science, companies are able to get business understanding of customer churn, develope and implement predictive model to predict future customer churn probability, then engage and act based on the result of analysis. 
## Churn Manage with Data Science:
### Capture & Analyze
Identify data requirements and explore data availability
Requeuest and extract data required to build a model
Aggregate, clean and standadize data in disired format for model
### Report & Predict
Business analytics of standadized data
Predictive model design
Development and implementation of predictive model
### Engage & Act
List of churn drivers / KPIs for trackign and monitoring
A generated list of recommended subscribers for targetedchurn campaigns
Recommendations on monthly churn initiatives 

# In this Project
## Business Need: 
with collected data, apply data science techniques to understand customer churn behaviors and build a predictive model to predict the probablity of future customer churn. 

## Data Acquisition
Data is collected and ready to use. The data is taken from Kaggle Customer Churn Competition
Data Srouce: https://www.kaggle.com/datasets/blastchar/telco-customer-churn
## Data Preparation 
Data is checked for dimension, uniqueness, columns type and meaning, and missingness. 
Univariate and Bivariate analysis are performed to visualize predictors and get initial data insights. 
Data is splitted into train and test set with stratified sampling, with categorical features tranformed by one-hot-encoding and numerical features standadized to same scale. 

## Model Training & Validation
1.	Construct baseline model with Logistic Regression Classifier, K Nearest Neighbors, and Random Forest Classifier. Applied 5-fold Cross Validation, models evaluated on Accuracy, Precision, and Recall.
2.	With highly imbalanced data, use SMOTEENN package to resample and transform the dataset into a more balanced dataset. 

## Testing & Evaluation
Baseline model results showed Logistic Regression and Random Forest performed better, thus drop KNN. 
1.	Use Grid Search to Find Optimal Hyperparameters   
Logistic Regression:  
  •	L1, L2 regularization  
  •	C = 1/lambda, weight of L1/L2  
Random Forest:   
  •	N_estimators: number of trees     
  •	Max_depth: It governs the maximum height upto which the trees inside the forest can grow. as we increase the depth of the tree the model accuracy increases upto a certain limit but then it will start to decrease gradually because of overfitting in the model.     

## Deployment & Inference (Work in Progress)  
FLASK is used to deploy the best model. FLASK API is created and UI will be used to take future input, a churn probability will be produced. 
