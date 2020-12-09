Metis Data Science Bootcamp Project 5

Project Title: Bike Sharing: Smart Solution For Traffic Congestion

I use time series analysis to analyze a potential smart solution, a Bike Sharing System, for the on-going traffic problems in the city of Chicago.

In 2019, congestion in Chicago was the second-worst in the country—up from third place in 2018. According to data released by the city, Uber and Lyft trips in Chicago increased 271 percent between 2015 to 2018. More than half of all car trips in Chicago were less than three miles and 22 percent were less than one mile. This high percentage of shorter trips suggest that the city could benefit from bikes as a way to replace traffic congestion.

In addition to the 2nd worst traffic in the US, Chicago ranks 10th for the most congested city in the world. On average, Chicago’s automobile commuters wasted 145 hours sitting in traffic in 2019 which is an an increase  from the 2018 figure of 138 hours. In terms of lost economic productivity, road congestion costs drivers over $2,000 last year.

The bike share data was collected from [divvybikes.com](https://divvybikes.com) and the traffic data was collected from Chicago’s Open Data Portal [data.cityofchicago.org](https://data.cityofchicago.org). 

Both datasets ranged form 2013-2018. The Divvy dataset had 22 million rides and the Chicago traffic dataset had 19 million records. That was too much data for my local machine so I stored and pulled the data from Google Cloud Platform. For Time Series Analysis and Forecasting, I started by analyzing bike share data with ARIMA and then compared the bike share data to the traffic congestion data with Facebook’s Prophet. For Data Visualizations, I used Tableau.

To help understand the accuracy of the forecast, I compared predicted bike share to actual bike share, and set the forecasts to start on Jan 1, 2017 until the end of the data midway through 2018. And so what you’re seeing in the line plot is the observed values compared to the rolling forecasted predictions. 

To measure forecast accuracy, I experimented with multiple KPIs and chose Mean Absolute Percentage Error. The MAPE indicates that the average difference between the predicted trip duration and the actual trip duration is 22.94%.

- Divvy Bike Share analysis showed that the data had an overall upward trend and seasonal fluctuations. 
- Chicago Traffic Congestion analysis showed that the data has an overall downward trend and seasonal fluctuations. 

This is something Divvy should keep their eye on. If this prediction holds Divvy will need to prepare operationally for the increase in demand. They could compete with ride share apps by positioning their docks throughout neighborhoods where pick ups and drops offs are frequent as well as focus their marketing campaigns on the benefits of inner city last mile commuting.

Big data to the rescue -- applying big data to create intelligent transportation systems is key to solving urban mobility problems. Data and analytics on traffic and population movement help city planners and engineers make data-based decisions to prioritize spending in order to maximize benefits and reduce costs.

### Files
[TimeSeriesFinal](/Users/jbpatty/project-5/TimeSeriesFinal.ipynb) shows the use of ARIMA and Facebook Prophet for an end-to-end time series analysis and forecasting with Python

[DivvyMerge](/Users/jbpatty/project-5/DivvyMerge.ipynb) and [TrafficMerge](/Users/jbpatty/project-5/TrafficMerge.ipynb) show the process of loading, cleaning, and merging 22 million rows of Divvy Bike Share rides and 19 million rows of Chicago traffic congestion records
