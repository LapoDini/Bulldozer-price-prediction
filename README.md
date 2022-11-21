# Bulldozer-price-prediction
This project aims to train a model to predict the price of heavy machines. We perform a brief EDA to find some insight, after that we manipulate the dataset (filling in missing values, and converting categories into numbers) and then we trained a model to predict the final price. 

## Data
The dataset was provided from Kaggle: https://www.kaggle.com/competitions/bluebook-for-bulldozers/data

This dataset has more than 400000 samples and more than 50 features, and a data dictionary is provided here: https://docs.google.com/spreadsheets/d/e/2PACX-1vTbZNhQwWedzw6y1VFqhsvfJo3rtyzen62a6G0rnwufZo9FAtbiO3qO4xbAGmANWQT9jDUg6N_E_knw/pubhtml

## Exploratory Data Analysis
https://github.com/LapoDini/Bulldozer-price-prediction/blob/main/bulldozer-price-EDA.ipynb

* Loading dataset and parsing Date and Time features
* Exploring the dataset to find information
* Visualizations


![download](https://user-images.githubusercontent.com/109316190/203017369-2dfe3529-a8f7-453a-b3b8-d5f2900377e1.png)


![download](https://user-images.githubusercontent.com/109316190/203017546-a30f6e9d-deb3-424b-a7b9-dcd26c375d49.png)


![download](https://user-images.githubusercontent.com/109316190/203017767-a4b8b283-69b5-4375-a85b-8742a0940e58.png)


![download](https://user-images.githubusercontent.com/109316190/203017815-98d724cc-0a6f-4cd3-b8c7-4a67cc961ed3.png)


## Modelling
https://github.com/LapoDini/Bulldozer-price-prediction/blob/main/Modeling.ipynb

In this notebook, we are training a model to predict the sale price of heavy construction equipment.

### Data Wrangling
* Load the parsed dataset from the eda
* Sorting the dataset by Year of Sale
* Filling numeric values with the mean 
* Convert non-numerical features in Category, using pandas API
* Convert category into number, using the category code provided by pandas API. 

### Modelling
After that, we start modelling: we choose a Random Forest Regressor from Scikit-Learn library.
We decide to evaluate our model performance with three different metrics

* R2 Score
* Mean Absolute Error
* Root Mean Log Squared Error

We see that the performance of our model is quite good but could be improved. 
We would like to try tuning our model with GridSearchCV and see if this will improve our model performance.
After that, we would like to try another model like Lasso or ElasticNet.
