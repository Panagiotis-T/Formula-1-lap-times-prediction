# Formula-1-lap-times-prediction
In this project the lap times of formula 1 drivers (21 drivers in total) in a particular race, are modeled.
An initial OLS model is used to predict the parameters of the model and form there the forecasted lap times including a measure of uncertainty.
In continuation, the parameters are estimated using WLS after assuming some correlation between the different laps of the same driver.
In the end, the optimal covariance matrix is found using the relaxation algorithm to estimate the correlation and 3 other parameters related to the first laps, laps with pit stop and laps following a pit stop.
The data, along with data from other races, is publically availabe at: https:
//www.kaggle.com/rohanrao/formula-1-world-championship-1950-2020/version/13?select=lap_times.csv.
