# Relative Humidity prediction based on Gases concentration and Temperature available

![Rain](Rain.png)

## Overview
1. Humidity prediction is one of the important aspect in weather prediction analysis to find out temperature and rain precipitation predictions.
2. This project is a regression model that will try to predict relative humidity (humidity %) in the given area using gases concentration and temperature available in that particular area.  
3. The dataset contains 9358 instances of hourly averaged responses from an array of 5 metal oxide chemical sensors embedded in an Air Quality Chemical Multi-Sensor Device.
4. The device was located on the field in a significantly polluted area, at road level, within an Italian city. Data were recorded from March 2004 to April 2005.
5. Ground Truth hourly averaged concentrations for CO, Non-Metanic Hydrocarbons, Benzene, Total Nitrogen Oxides (NOx), and Nitrogen Dioxide (NO2) were provided by a co-located reference certified analyzer. 
6. Missing values are tagged with -200 value.

## Dataset 

The dataset can downloaded from [here](https://archive.ics.uci.edu/ml/datasets/Air+Quality).

## EDA and Feature Engineering

1. Read and view the data file.
2. NA values are filled as -200. So replace -200 with np.NaN
3. The feature column NMHC(GT) contains almost 90% NA values so we will delete it.
4. Delete all the rows with NA values.
5. Let us make the year, month and day as 3 new features from the Date column.
6. Extract Hour from time and make it as a new feature. As humidity depends upon time and season these features are very imp.
7. Now delete the Date and Time column.
8. As our target is predicting RH(Relative Humidity), we must drop AH(Absolute Humudity).

The Best Results among different values of alpha are:

1. Linear Regression with L2 regularization (ridge regression) for alpha=10\
1.1. Training Accuracy: 0.71\
1.2. Testing Accuracy: 0.72

2. Polynomial Regression (degree=2) with L2 regularization (ridge regression) for alpha=1\
2.1. Training Accuracy: 0.85\
2.2. Testing Accuracy: 0.81

3. Polynomial Regression (degree=3) with L2 regularization (ridge regression) for alpha=1\
3.1. Training Accuracy: 0.89\
3.2. Testing Accuracy: 0.75


