# Predict the Housing Prices in Ames (Kaggle)
https://www.kaggle.com/c/house-prices-advanced-regression-techniques

#### Dataset
Data set describing the sale of individual residential property in Ames, Iowa
from 2006 to 2010. The data set contains 2930 observations and a large number of explanatory
variables (23 nominal, 23 ordinal, 14 discrete, and 20 continuous) involved in assessing home
values. 

### Target
Analyze the housing data collected on residential properties sold in Ames, Iowa between 2006 and 2010. The goal is to predict the final price of a home with those explanatory variables.

Main file: Name my main file as mymain.ipynb

## Step and Process 


### Load the dataset
Load the dataset Ames_data.csv and split the data into 70% training and 30% testing dataset

### Data preprocessing
Because I try to use one-hot encoding later. In order to decrease the number of categories. First I delete the column if its categories exceed 15. Training dataset and test dataset would get differ- ent number of columns while doing one-hot encoding, so I need to align the X_train and X_test together to get the same number of column. Then I use imputer to replace the Nan value by the mean value.

- Use label encoder to deal with categorial variable
I’ve tried to use label encoder first, but it turns out a bad predicted result compared to one hot encoding.

### Model prediction
- XGboost
XGBoost is an optimized distributed gradient boosting system designed to be highly efficient, flexible and portable. It implements machine learning algorithms under the Gradient Boosting framework.

Root-Mean-Squared-Error (RMSE) for XGBoost model is 0.1288

- Gradient Boosted Regression
I’ve tried random forest algorithm in the beginning, but the RMSE was still high. So I use GBR which is similiar to XGboost

Root-Mean-Squared-Error (RMSE) for GBRT model is 0.1263

