# Relative Humidity prediction based on Gases Concentration and Temperature available

Humidity prediction is one of the important aspect in weather prediction analysis to find out temperature and rain precipitation predictions.

This is project is a regression model which will try to predict relative humidity (humidity %) in the given area using gases concentration and temperature available in that particular area.  

The dataset contains 9358 instances of hourly averaged responses from an array of 5 metal oxide chemical sensors embedded in an Air Quality Chemical Multi Sensor Device.

The device was located on the field in a significantly polluted area, at road level,within an Italian city. Data were recorded from March 2004 to April 2005.

Ground Truth hourly averaged concentrations for CO, Non Metanic Hydrocarbons, Benzene, Total Nitrogen Oxides (NOx) and Nitrogen Dioxide (NO2) and were provided by a co-located reference certified analyzer. 
 
Missing values are tagged with -200 value.

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



The dataset can downloaded from [here](https://archive.ics.uci.edu/ml/datasets/Air+Quality).
