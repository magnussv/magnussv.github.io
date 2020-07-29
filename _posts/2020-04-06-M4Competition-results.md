---
layout: post
title: The absence of evidence-based success for pure machine learning methods in time series forecasting 
subtitle: Results from the M4 competition
bigimg: /img/crystal-ball-see-the-future.jpg
tags: [M4 Competition, time series forecasting, machine learning, statistics]
---
Machine learning, sometimes overgeneralized called simply *AI*, is commonly described as the holy sauce for most things within prediction making. Build your machine learning model with training data, and use the model you just built to predict an unknown event with unprecedented accuracy. Turns out it is not always as simple as that.

Results from the [M4 Competition](https://www.sciencedirect.com/science/article/pii/S0169207019301128), where scientists and practitioners could send in predictions for 100 000 time series, indicate that pure machine learning methods perform rather poor. The more classically based statistical methods, like exponential smoothing and ARIMA, still have the edge over the machine learning counterparts when predictions from single methods are compared. However, you should seldom use predictions from a single model as your final prediction; this is a finding that has been validated over and over again for at least the past couple of decades. Below are the most interesting findings from the M4 Competition.


**Combined forecasts are still King**
It is more or less always, in the longrun, a good idea to combine forecasts from multiple methods into one final combined forecast. You will likely get the highest forecast accuracy this way. How you decide to combine them may differ, and there are better and worse ways to do this, but most of them are better than not combining at all.


**Go hybrid of you want to reach state-of-the-art accuracy** 
The winning method was [Smyl's hybrid approach](https://www.sciencedirect.com/science/article/pii/S0169207019301153) that utilized both statistical and machine learning features. Make no mistake, this is a truly hybrid approach, not a combination of pure statistical and machine learning forecasts. The precision of the submitted prediction intervals where amazing as well. I view this method as the most innovative and brilliant output from the whole competition. This will probably be a major building block in both future practice and development work.


**Use information from multiple time series to predict individual ones**
If you can get a hold on time series that, in some way, are similar to the one you are doing a forecast on, then you may use forecasts from these time series to decide the most effective way of forecasting and/or selecting ways to combine forecasting methods. The authors of the top methods did this.


**The poor performance of pure machine learning methods**
As pointed out earlier, there is no advantage of using pure machine learning methods in time series. Yet at least. More tuning and innovation are needed to understand why they often fail to produce a good outcome. Is it caused by over-fitting, or is it due to the obvious lack of a large sample of training data when it comes to time series in general? Or is it maybe the non-stationarity in the data? Time will likely tell, and improvements will likely be made. However, for now, we don't really understand the true potential and limitation of machine learning methods within the field of time series forecasting.