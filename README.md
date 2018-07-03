# Answers

link to the live site: https://burcukolbay.github.io/answers/

For the data source part, "room_users" table is used as the middle one to be connected to the other two tables: "rooms" and "users". "inner" join is used in order to have the connection based on "user_id" and "room_id". It increases the data into 49 observations. It is done in this way unless otherwise stated. 

# Question 1: 
Create a Tableau visualization in which a daily time series for user acquisition is plot. Create filters for days. Now, suppose we want to aggregate to different time horizons. Create a filter that selects days, months or weeks as time aggregation.

## Solution 1.1: 
<iframe src="https://public.tableau.com/views/assingment_badi/Question1-dayfilters?:showVizHome=no&:embed=true" width="1000" height="500"></iframe>

The days selection is added on the right pane. This can help us to one who wants to see the days individually or in an aggregated way. Number of records are represented using hour distribution.

## Solution 1.2:

<iframe src="https://public.tableau.com/views/assingment_badi/Question1-aggregation?:showVizHome=no&:embed=true" width="1000" height="500"></iframe>

The aggregation selection is added on the right pane. Depends on the need, one can choose daily, weekly and monthly aggregation.

# Question 2:
Repeat the exercise with rooms.

## Solution 2.1:
<iframe src="https://public.tableau.com/views/assingment_badi/Question2-dayfilters?:showVizHome=no&:embed=true" width="1000" height="500"></iframe>

The day selection is added on the right pane.

## Solution 2.1:
<iframe src="https://public.tableau.com/views/assingment_badi/Question2-aggregation?:showVizHome=no&:embed=true" width="1000" height="500"></iframe>

The aggregation selection is added on the right pane. Depends on the need, one can choose daily, weekly and monthly aggregation.

# Question 3:

Suppose we are interested in knowing how the market is distributed (supply and demand). Create a Tableau visualization in which you plot the difference between supply and demand (listers and seekers). First on aggregate and then over the time series.

## Solution 3:

The data consists of the room information and the user who posted the room. There is no information for the renter. It does not make sense to do supply demand analysis. 

In the case that we "suppose" that we have the necessary information, it is not still feasible to do it. The given data instance is not available to have a real scenario for supply-demand gap. Because the dates come from room creation are from August, September, October, November and December 2015. On the other hand, the user records are from 2017. The instance of the data should have been correct in order to do this analyses!

In the case that it was possible, I would use supply deman floating gap bars to illustrate.

# Question 4:

One of the most important things when assessing rooms is the geolocation of such rooms. Create a Tableau visualization showing the number of rooms per country, city, and neighbourhood. Also, you must allow for date selection. Create filters for all data fields.

## Solution 4:

<iframe src="https://public.tableau.com/views/assingment_badi/Question4-theroomnumberscountrycityneighborhood?:showVizHome=no&:embed=true" width="1000" height="500"></iframe>

Since the inner join is taken the other countries are not shown in the plot. However, the country selection is done on the right pane.  
