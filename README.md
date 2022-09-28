# Analyzing Ride Sharing Data by City Type
---
## Analysis Overview

### Determining Analysis Requirement

Pyber is an app based ride sharing company that provides its services across multiple cities. When distilling Pyber's service offering through geographic segmentation, Pyber has segmented its markets into Urban, Suburban and Rural regions. Under each segmented market, lies multiple cities which utilizes the services offered by Pyber.

Considering the above regional segmentation, Pyber has extracted rider and city data for a period of 4.5 months (ranging from 01st January 2019 to 08th May 2019). The extracted data can be used to understand pricing, rider and driver behaviour across the regional segments.

Analysing the data will provide us with insight on how Pyber can fine tune thier service offering to offer a more consumer centric product across regional segments.

The sections below highlight the approach and analytical outputs from the Python script utilising pandas and matplotlib libraries.

## Analysis Results

### Regional variances seen in ride sharing Data by City Type

#### Comparing Total Rides - City Type

![PyBer_total_rides](/Analysis/PyBer_total_rides.png)

As demonstrated in the above line graph, ridership amongst regional segments differ quite significantly among the Rural, Suburban and Urban regions. 

Our data shows, the Total Rides in Rural regions stand at only 125 rides during the analyzed period. Copared to Rural, we see ridership in Suburban regions having 5 times the Rural ridership at 625 rides, and Urban ridership more than 2.5 times that of Suburban ridership at 1,625 rides.

The above data demonstrates significant differences and we need to determine what may be the factors driving disparities. Whether it can be identified through our analysis, or if other macro-economic factors may be effecting the outcomes.

#### Comparing Total Drivers - City Type

![PyBer_total_drivers](/Analysis/PyBer_total_drivers.png)

The Total Drivers data demonstrates a similar pattern to Total Rides. The Rural Driver Count only stands at 78 drivers, whilst Suburban and Urban Drivers are 490 and 2405 respectively.

Despite showing similar differences, in terms of trendline, if we look at the data closely, we can come to the following conclusions;

1. Despite Suburban Region having 5 times the ride count of Rural Region, the driver count for Suburban Region is almost 6.5 times greater than the Rural Region.
2. Similarly, despite Urban Region having 2.5 times the ride count of Suburban Region, the driver count for Urban Region is almost 5 times greater than the Suburban Region.

Given the above, we see a alack of proportionality across regions when considering total ridership and drivers serving each region.

1. When comparing Rural and Suburban, there are more drivers serving Suburban Region compared to it's relative ridership.
2. When comparing Suburban and Urban, there are more drivers serving Urban Region compared to it's relative ridership.

We see that the Suburban and Urban markets are facing an over supply of drivers whilst the Rural market is having insufficient supply in relative terms.

#### Comparing Total Fare ($USD) - City Type

![PyBer_total_fare](/Analysis/PyBer_total_fare.png)

Given the high ridership and high driver supply, we see a similar trend in terms of total fare across regions. The Total Fare data indicates the following;

1. Total Fare - Rural City Type is $USD 4,327.93
2. Total Fare - Suburban City Type is $USD 19,356.33
3. Total Fare - Urban City Type is $USD 39,854.38

Looking at the total fare data in isolation, does not tell much of a story. But, we can derive average fare data per ride and driver to assess market conditions in a more detailed manner.

#### Comparing Average Fare (Ride) - City Type

![PyBer_avg_fare_ride](/Analysis/PyBer_avg_fare_ride.png)

The average fare by ride is inversely proportionate to the total rides. The more rides per region, the lower the average fare. The above trend results in the average fare by ride across our regions to be as follows;

1. Average Fare (Ride) - Rural City Type is $USD 34.62
2. Average Fare (Ride) - Suburban City Type is $USD 30.97
3. Average Fare (Ride) - Urban City Type is $USD 24.53

Considering the differences in average fare (ride) by regions, we can consider two of the following action points if we are to seek pricing parity;

1. Influence the demand for ridership in the Rural and Suburban regions.
2. Incetivize drivers from the Suburban region to serve the Rural region and the Urban drivers to serve the Suburban region.

#### Comparing Average Fare (Driver) - City Type

![PyBer_avg_fare_driver](/Analysis/PyBer_avg_fare_driver.png)

Similar to the average fare by ride, the averager fare by driver is also inversely proportionate to the total drivers. The more drivers per region, the lower the average fare. The above trend results in the average fare by drivers across our regions to be as follows;

1. Average Fare (Driver) - Rural City Type is $USD 55.49
2. Average Fare (Driver) - Suburban City Type is $USD 39.50
3. Average Fare (Driver) - Urban City Type is $USD 16.57

Despite the average fare per driver following a similar trendline to that of the average fare by ride (we see that the downward slope is much more aggressive on that of the average fare per driver.

1. Difference in Rural and Suburban regions for average fare per ride is 3.65 $USD, but the difference in average fare per driver is 15.99 $USD.
2. Similarly, difference in Suburban and Urban regions for average fare per ride is 6.44 $USD, but the difference in average fare per driver is 22.93 $USD.

As indicated above when comparing total rides and total drivers, the proportional disparities seen in the average fare by drivers is much larger than that of the average fare by ride.

The above indicates that the demand side for of rides for our rideshare services are sustainable, but the supplyside of drivers needs to be corrected to avoid loss of ridership and prevent disincentivization of drivers.

## Business Recommendations

#### Improve demand in rural and suburban ridership

#### Open up the market for drivers to serve cross regionally

#### Incentivize drivers to serve rural markets