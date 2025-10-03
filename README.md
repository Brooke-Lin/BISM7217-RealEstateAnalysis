**Real Estate Market Analysis**
-
**Overview**
-

This project is a university coursework. It explores real estate market data to understand property trends and predict whether properties will have a high or low number of days on the market. The analysis involves data cleaning, clustering, and applying multiple machine learning models for prediction.  

The goal of this project is to provide insights into property characteristics that influence market behavior and identify the best predictive model for days on market.

**Data Cleaning Steps**
-
* Removed outliers in `beds`, `baths`, and `parks` 
* Dropped irrelevant columns (`unnamed: 0.1`, `unnamed: 0`, `description`, `address`, `state`, `postcode`)
* Removed `listed_date` and `sold_date` as datetime types are not used in modeling 
* Dropped `listed_price` due to 70% missing values 
* Removed duplicate property records 
* Dropped null values in `average_days_on_market` and `average_median_price` to maintain data accuracy 
* Predicted missing values in `property_size` using linear regression 
* Converted all features to numerical data types for model compatibility

**Exploratory Analysis**
-
* Applied clustering techniques: KMeans and Agglomerative Clustering  
* The Elbow method suggested 3 clusters as optimal for the dataset


**Model Building**
-
Five machine learning models were used to predict the target label (`days on market`):  

1. **Decision Tree**: Maximum depth set to 3, trained with 80% data  
2. **Random Forest**: Ensemble of decision trees, best-performing model  
3. **Artificial Neural Network (ANN)**: Multi-layer perceptron with 1 hidden layer of 25 neurons, trained for 500 iterations
4. **K-Nearest Neighbors (KNN)**: k=5 nearest neighbors used for prediction  
5. **Naive Bayes (NB)**: Gaussian distribution assumption for features

**Key Findings**
-
* Random Forest was the most accurate and reliable model for predicting days on market  
* Important features influencing market days include:  
  * Number of baths  
  * Property size  
  * Average days on market  
  * Property sub-classification  

* Data cleaning and feature engineering significantly improved model performance



