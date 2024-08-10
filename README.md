Project Summary: NOAA Weather Data Analysis for JFK Airport
Objective:
The primary goal of this project is to analyze weather data from JFK Airport to predict precipitation levels using various climatological variables. This analysis is crucial for understanding weather patterns that could impact flight operations, particularly the likelihood of precipitation, which can cause delays.

Dataset Overview:
The dataset used is a subset of the NOAA Weather Dataset from JFK Airport. It contains 5,727 hourly observations across 9 variables, including:

DATE: Date of observation.
HOURLYDewPointTempF: Dew point temperature in Fahrenheit.
HOURLYRelativeHumidity: Relative humidity percentage.
HOURLYDRYBULBTEMPF: Dry bulb temperature in Fahrenheit.
HOURLYWETBULBTEMPF: Wet bulb temperature in Fahrenheit.
HOURLYPrecip: Precipitation in inches.
HOURLYWindSpeed: Wind speed in mph.
HOURLYSeaLevelPressure: Sea level pressure in inches of mercury.
HOURLYStationPressure: Station pressure in inches of mercury.
Project Structure:

Data Import and Setup:

Imported necessary libraries (Tidyverse, Tidymodels).
Downloaded and unzipped the NOAA weather dataset.
Loaded the dataset into the project.
Data Preprocessing:

Selected relevant columns: HOURLYRelativeHumidity, HOURLYDRYBULBTEMPF, HOURLYPrecip, HOURLYWindSpeed, HOURLYStationPressure.
Cleaned up the HOURLYPrecip column by replacing T (trace) with 0.0 and removing characters like "s" that indicated snow.
Converted HOURLYPrecip to a numerical type.
Renamed columns to more intuitive names (e.g., HOURLYRelativeHumidity to relative_humidity).
Exploratory Data Analysis:

Split the data into training (80%) and testing (20%) sets.
Visualized the distribution of variables using histograms.
Linear Regression Modeling:

Created simple linear regression models to predict precipitation (precip) based on individual predictors: relative_humidity, dry_bulb_temp_f, wind_speed, and station_pressure.
Visualized each model with scatter plots and regression lines.
Model Improvement:

Created more advanced models by adding polynomial components and combining multiple predictors (Multiple Linear Regression).
Evaluated model performance using metrics like R-squared and RMSE.
Model Comparison:

Compared different models' performance on the test set to identify the best model.
Created a summary table to compare training and testing errors across models.
Concluded the best-performing model based on test set performance.
Conclusion:
The project successfully analyzed and modeled the weather data to predict precipitation at JFK Airport. The model comparison step helped identify the most effective model for predicting precipitation, which can be used to inform decisions related to flight operations and delay management.
