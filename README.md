# Seoul-Bike-Rental-Prediction-
Python_For_Data_Analysis_Seoul_Bike
# Feature matrix creation
On the client side, it will be ask to create a matrix of features to predict. Each row is a list of ordered features as following :

Feature	Format
Date	dd/mm/yyyy
Hour	int
Temperature	°C
Humidity	%
Wind speed	m/s
Visibility	10m
Dew point temperature	°C
Solar Radiation	MJ/m2
Rainfal	mm
Snowfall	mm
Seasons	{"Winter", "Autumn", "Spring", "Summer"}
Holiday	{"Holiday", "No Holiday"}

# Run the API
We can run this server from terminal running the python deployed_model.py or python3 deployed_model.py according to your OS and python version.

# Request the API
From the preprocessing.py file I recreate the preprocessing function :

set holiday feautre as boolean
extract time features
trasnform meteorological arguments
complete preprocessing with one hot encoding on categorical feautures and norm/standardization on numerical ones``

# Objectives

From kaggle dataset was missing so I decided to choose the Seoul bike sharing demand dataset dataset found on Machine Learning Repository.

# Abstract

The dataset contains count of public bikes rented at each hour in Seoul Bike haring System with the corresponding Weather data and Holidays information.

Data Set Information

Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes. The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.

The objective of the notebook is to analyze the dataset I get assigned and to make from there:

1- A powerpoint explaining the ins and outs of the problem, my reflections on the question raised, the different variables I have created, how the problem fits into the context of the study. In this case, I will try to predict the number of bikes rented in Seoul based on temporal and meteorological features.
2- A python code :
                  Data-visualization - showing the link between the variables and the target
                  Modeling - take scikit-learn and try several algorithms, change hyper parameters, make a search grid, compare results of my models in graphs.
3-Transformation of the model into a Django of Flask API

#Date: Extract date informations :

-year number
-month name
-day number
-week day name
-working day condition

# Selected model

Model comparison
For each following models I performed the same process :

-LinearRegression
-ElasticNet
-HuberRegressor
-BayesianRidge
-ARDRegression
-KNeighborsRegressor
-RandomForestRegressor

For each dataset in {transformed dataset, untransformed dataset}: For each model :

Grid search on hyperparameters (if needed) ON THE TRAINING SET
Get the best hyperparameters for the model
Compute the RMSE on the prediction ON THE TEST SET
