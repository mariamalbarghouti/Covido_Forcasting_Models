# Covido_Forecasting_Models
These Models For My Garaduation Projecet. I have created these three models for forecasting the next 7 days new, recovery and death cases caused by covid-19 virus. 

I have singled out Egypt by these Models.
I have get the data-set using these APIs:
- [Confirmed](https://api.covid19api.com/country/egypt/status/confirmed/live)
- [Recovery](https://api.covid19api.com/country/egypt/status/recovery/live)
- [Death](hhttps://api.covid19api.com/country/egypt/status/death/live)
 
I have used [FacebookProphet](https://facebook.github.io/prophet/) For Forcasting.

## Why Fbprophet?
Facebook developed an open sourcing Prophet, a forecasting tool available in both 
Python and R. It provides intuitive parameters which are easy to tune. Even someone 
who lacks deep expertise in time-series forecasting models can use this to generate 
meaningful predictions for a variety of problems in business scenario.

> “Producing high quality forecasts is not an easy problem for either machines or for most 
analysts. We have observed two main themes in the practice of creating a variety of 
business forecasts:
• Completely automatic forecasting techniques can be brittle, and they are often too 
inflexible to incorporate useful assumptions or heuristics.
• Analysts who can product high quality forecasts are quite rare because forecasting 
is a specialized data science skill requiring substantial experience.”

## Highlights of Facebook Prophet 
- Very fast, since it is built in Stan, a programming language for statistical inference 
written in C++.
- An additive regression model where non-linear trends are fit with yearly, weekly, 
and daily seasonality, plus holiday effects: 1. A piecewise linear or logistic growth 
curve trend. Prophet automatically detects changes in trends by selecting 
changepoints from the data 2. A yearly seasonal component modeled using 
Fourier series 3. A weekly seasonal component using dummy variables 4. A userprovided list of important holidays.
- Robust to missing data and shifts in the trend, and typically handles outliers.
- Easy procedure to tweak and adjust forecast while adding domain knowledge or 
business insights.

## Facebook Prophet Forecasting Model Uses

The Prophet uses a decomposable time series model with three main model 
components: trend, seasonality, and holidays. They are combined in the following 
equation:

*y(t)= g(t) + s(t) + h(t) + εt*

- g(t): piecewise linear or logistic growth curve for modeling non-periodic changes 
in time series
- s(t): periodic changes (e.g. weekly/yearly seasonality)
- h(t): effects of holidays (user provided) with irregular schedules
- εt: error term accounts for any unusual changes not accommodated by the model
- Using time as a regressor, Prophet is trying to fit several linear and nonlinear 
  functions of time as components. Modeling seasonality as an additive component 
  is the same approach taken by exponential smoothing in Holt-Winters technique . 
  Facebook Prophet is framing the forecasting problem as a curve-fitting exercise 
  rather than looking explicitly at the time-based dependence of each observation 
  within a time series.

## The accuracy were

![Accuracy](https://firebasestorage.googleapis.com/v0/b/fluttertrail.appspot.com/o/c.png?alt=media&token=41a2c894-4ed4-4572-a8e6-4df6242dc1da)

