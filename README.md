# Formula-1-lap-times-prediction
In this project, the lap times of Formula 1 drivers in a particular race, are modeled. An initial OLS model is used to predict the parameters of the model and from there the forecasted lap times including a measure of uncertainty are found. 
For some of the drivers, it is clear that the GLM model results in large autocorrelations
in the residuals, with the model systematically giving too small predictions prior to the pitstop and too large predictions after the pitstop. Furthermore, for all drivers, even when correcting for the spikes in lap times, the variance is still larger for these laps. These phenomenons call for WLS estimates of the parameters, based on correlations between lap times for each particular driver, and increased variance during the events coursing the spikes in lap times.
In continuation, seeing that the variance is larger for some time steps, the parameters of the model are re-estimated after assuming that the standard deviation is larger by a factor during the laps for which a particular driver made a pit stop.
Lastly, the optimal covariance matrix is found using the relaxation algorithm to estimate the correct value of correlation and 3 other parameters related to the events coursing the spikes in lap times (first laps, laps with pit stop, and laps following a pit stop).
The data, along with data from other races, is publically availabe at: https:
//www.kaggle.com/rohanrao/formula-1-world-championship-1950-2020/version/13?select=lap_times.csv.
