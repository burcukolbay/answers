# Answers

link to the live site: https://burcukolbay.github.io/answers/

In the file that is sent by Leticia Castro, the keys to access were as follows:

Public IP address:
35.190.223.80

Port: 3306

User name:
readerENOtotn1c7OBf7Yf

In the documentation, it is mentioned that there are 3 tables. However, after I connected with the keys above, I receive 4 tables. The target tables (3) and one named as "recommendations". The "recommendations" table is not used. 

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

# Question 5:

We are interested in the number of rooms per lister. Create a Tableau visualization in which the distribution of rooms per user is plot. What's the main insight you take from this visualization?

## Solution 5:

<iframe src="https://public.tableau.com/views/assingment_badi/Question-5?:showVizHome=no&:embed=true" width="1000" height="500"></iframe>
https://public.tableau.com/views/assingment_badi/Question-5?
In the inner join version for room and user data sets, although we see that the users tend to have only one room, there are some users related to two rooms. In a future analyses, this issue can be focused on in order to see if the users are connected to more than one room when the dates of two creations are close. If the gap between two creation dates of rooms for the same user is not so short, then it might be considered in such a way that the user has a new place to live. Otherwise, there is an important issue to detect the swindlers. In the data we work on for this assignment, and its inner join version, the maximum number of rooms per user is 2. However, I am pretty sure that there will be some users with several rooms in the whole original data.

# Question 6:

Imagine that we wanted some insights about gender, age, and occupation of our users. Create a Tableau visualization that assess the distribution of users over these features. Try to avoid pie charts.

## Solution 6:

<iframe src="https://public.tableau.com/views/assingment_badi/Question-6?:showVizHome=no&:embed=true" width="1000" height="500"></iframe>
                                                                                                                                      
First of all, the ages are calculated from the "Calculated Field". The difference between the birthdate and today is taken. Then, the age bins are created for each 5 year. Two more "Calculated Field"s are used for "Female Population" and "Male Population". Gender, occupation, and age bins are represented in one Tableua sheet. The blue and red colors are given to the women and men populations respectively. Occupation distribution using age bins are colored depends on the occupation. In the inner join version for user and room data sets, there is no user with "Both(3)" occupation option. There is only students and workers. The green and orange colors are given respectively.                                                                                                                                       
# Question 7:

Giving only the room’s latitude and longitude it’s possible to predict an accurate price? There are other factors(features/variables) that can explain the price? How? Why?

Having only the coordinates is not good enough for price prediction. In research, there are some studies that used geospatial coordinates for house price prediction. However, the geospatial coordinates are used in order to detect the country, cit, district, neighborhood, etc. It is useful to cluster the close geospatial coordinates in order to detect small parts of the city as the target area or their different characteristics. To be able to give more accurate answer, I should have had the whole data, not only a small sample. Then, I would check the features and their importance on estimating the price. 

The rest of the answer based on guesses and assumptions.

"city_id", "country_id", "neighborhood_id" are important for estimation since they could describe effects of the income, life standards, tourism attraction, etc. These effects can create or change the cities' or the neighborhoods' expensiveness. Thus, this expensiveness would have an effect on the rent prices. These three ID would not be in the model together necessarily. If there is a high correlation among these features, one or two of them will not be in the model. It requires bivariate statistical analysis. 

"Birth_date" could have an effect on the price. For instance, in Barcelona, the young or middle age people are looking for rooms mostly. Also they prefer to stay with the people in their age bin. If an older person is posting a room, it is more likely that he/she will not receive requests as much as the young/middle age listers do. It can cause a reduction of the room price in order to find a renter.  

"is_smoker" could have an effect on the price. However, it is not significantly obvious like "city_id", "country_id", "neighborhood_id" would have. Some room listers would like to have non-smoker housemates, and the rent could be higher since it promises a healtier environment. As my personal view, as a person who stays at a room in someone else's flat, and a person who seeks a room time to time, I did not see a significant difference on price between smoker and nonsmoker flats. Thus, it will probably will not have an impact on the price modeling, at least for Barcelona. 

For the "female_tenants", "male_tenants" and "biological_sex", I can repeat the assumption for "is_smoker". It can have an effect on the price that is declared by the seeker. However, it needs more analyses. It is still not s obvious like "city_id", etc. People can tend to stay with women because of the cleaning issue, etc. at flats. In this scenario, we can state the fact that it will be a bit more difficult to men to find a room than the women. So this issue can effect the prices as well.

"occupation" could have an effect as well. If I was a lister, and have my flat, I would prefer to have a renter who works. Because the renter will pay the rent montly without a problem, there will no Erasmus party at home, etc. In this scenario, in order to find the right person for my flat I could reduce the rent a bit since most of the room seekers in Barcelona are students. However, this is my personal choice. To see the other people choice, we need to do more analyses to understand if the other listers agree with me.


