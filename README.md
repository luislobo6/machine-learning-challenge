# machine-learning-challenge
Exoplanet Exploration


The Kepler Space Observatory is a NASA-build satellite that was launched in 2009. The telescope is dedicated to searching for exoplanets in star systems besides our own, with the ultimate goal of possibly finding other habitable planets besides our own. The original mission ended in 2013 due to mechanical failures, but the telescope has nevertheless been functional since 2014 on a "K2" extended mission.

Kepler had verified 1284 new exoplanets as of May 2016. As of October 2017 there are over 3000 confirmed exoplanets total (using all detection methods, including ground-based ones). The telescope is still active and continues to collect new data on its extended mission.



### After Exploring the CSV and reading the documentation

* The kepler_name have some values as NaN, so the better id/name for each planet is kepoi_name column
* koi_period - Orbital Period (days)- The interval between consecutive planetary transits
* koi_depth - Transit Depth (parts per million) - The fraction of stellar flux lost at the minimum of the planetary transit
* koi_srad - Stellar Radius (solar radii) - The photospheric radius of the star
* koi_steff - Stellar Effective Temperature (Kelvin) - The photospheric temperature of the star

https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html



### Polynomial Regression, Multiple Regression

With this exercise we could notice that we can estimate if a planet is a Candidate or a False Positive very efectively, with an MSE: 0.8770916548464863 and r2: 0.12300190457923421, just taking the values of the next data:
* koi_period
* koi_depth
* koi_srad
* koi_steff


### Random Forest

With this exercise we could define the importance of each variable of the previous exercise and we got that Orbital Period (days)- The interval between consecutive planetary transits is the most important variable to predict if a planet could be a candidate:
* koi_depth -> 0.31486729342021613
* koi_period -> 0.2861761313660855
* koi_srad -> 0.20219979540036148
* koi_steff -> 0.1967567798133368