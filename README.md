## Introduction

On January 27th 2021, the Washington Post reported 984 people were shot and killed by the police in 2020. It was also reported the rate at which black Americans were killed by police is more than twice as high as the rate for white Americans [ref](https://www.washingtonpost.com/graphics/investigations/police-shootings-database/). Amongst the killings was that of George Perry Floyd Jr, an unarmed black man that was reported been killed by an officer who knelt on his neck for 8mins and 46 seconds. This sparked an outrage in the US marked by weeks of unrest all over the country. This incident and many others has motivated the current president, Joe Biden to issue series of executive orders to address racial inequality in federal policy. 

## Project Objective
We aimed at applying time series anlysis techniques in order to forecast the number of deaths in the nearest future given the current and past deaths of US citizens by the police department in the USA.
## Methodology
### About the Data
The dataset contains 4851 every day killings by the US police from 2015-01-02 till 2020-06-15. It caputure information such as the name, manner of death, raace, armed etc. For our analysis we aggregated the data into weekly killings (287). <br>
To train our model, we use 90% of the data (258 obs) and left out 10% (29) for the test data set. 
### Modelling
After exploring the dataset, checking the ACF, PACF, detrending, several ARIMA models were tested on the train dataset and the model with the smallest aic was choosen. To check how well our model was doing, we calculated mean square error by using the final model to predict the the test observations. 
## Results
### Data Exploration
Looking at the various exploratory plots as seen below and also based on the values of ACF and PACF, we could see a slide downward trend detected in the time series plot. Also the values of ACF and PACF were not trailling off quicky at early lags. No form of seasonality was found and the data looks normally distributed. 
[Time Series plot]('Pics/fig1.png')
