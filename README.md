# Analyzing Ride Sharing Data by City Type
---
## Analysis Overview

### Determining Analysis Requirement

Pyber is an app-based ride sharing company that provides its services across multiple cities. When distilling Pyber's service offering through geographic segmentation, Pyber has segmented its markets into Urban, Suburban and Rural regions. Under each segmented market, lies multiple cities which utilizes the services offered by Pyber.

Considering the above regional segmentation, Pyber has extracted rider and city data for a period of 4.5 months (ranging from 01st January 2019 to 08th May 2019). The extracted data can be used to understand pricing, rider and driver behavior across the regional segments.

Analyzing the data will provide us with insight on how Pyber can fine tune their service offering to offer a more consumer centric product across regional segments.

The sections below highlight the approach and analytical outputs from the Python script utilizing pandas and matplotlib libraries.

## Analysis Results

### Regional variances seen in ride sharing Data by City Type

#### Comparing Total Rides - City Type

![PyBer_total_rides](/Analysis/PyBer_total_rides.png)

As demonstrated in the above line graph, ridership amongst regional segments differ quite significantly among the Rural, Suburban and Urban regions. 

Our data shows, the Total Rides in Rural regions stand at only 125 rides during the analyzed period. Compared to Rural, we see ridership in Suburban regions having 5 times the Rural ridership at 625 rides, and Urban ridership more than 2.5 times that of Suburban ridership at 1,625 rides.

The above data demonstrates significant differences, and we need to determine what may be the factors driving disparities. Whether it can be identified through our analysis, or if other macro-economic factors may be affecting the outcomes.

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
2. Incentivize drivers from the Suburban region to serve adjoining Rural region and Urban drivers to serve adjoining Suburban region.

#### Comparing Average Fare (Driver) - City Type

![PyBer_avg_fare_driver](/Analysis/PyBer_avg_fare_driver.png)

Similar to the average fare by ride, the average fare by driver is also inversely proportionate to the total drivers. The more drivers per region, the lower the average fare. The above trend results in the average fare by drivers across our regions to be as follows;

1. Average Fare (Driver) - Rural City Type is $USD 55.49
2. Average Fare (Driver) - Suburban City Type is $USD 39.50
3. Average Fare (Driver) - Urban City Type is $USD 16.57

Despite the average fare per driver following a similar trendline to that of the average fare by ride (we see that the downward slope is much more aggressive on that of the average fare per driver.

1. Difference in Rural and Suburban regions for average fare per ride is 3.65 $USD, but the difference in average fare per driver is 15.99 $USD.
2. Similarly, difference in Suburban and Urban regions for average fare per ride is 6.44 $USD, but the difference in average fare per driver is 22.93 $USD.

As indicated above when comparing total rides and total drivers, the proportional disparities seen in the average fare by drivers is much larger than that of the average fare by ride.

## Business Recommendations

The above analysis indicates that the demand for rides of rideshare services are underutilized, and the supply of drivers need to be corrected to avoid loss of ridership and prevent disincentivizing drivers.

The following recommendations are a starting point to balance demand and supply across regions (city types);

#### Improve demand in rural and suburban ridership

1. Total Ridership (Rural) - 125 Rides
2. Total Ridership (Suburban) - 625 Rides
3. Total Ridership (Urban) - 1,625 Rides

A key contributor to our analysis is to understand the population data across the selected regions. Based on the overall population, if we can determine the proportion of ridership, we may see that ride sharing services offered through Pyber may be underutilized.

Underutilization, can be driven by factors like under-population (not a sizeable market), lack of awareness or due to lack of supply, prices being too high to consider.

In the case of lack of awareness, we could consider running a few promotional campaigns targeting underutilized regions. And in the case of pricing being too high, we can offer usage bundles or promotional discounts to entice potential customers.

#### Open up the market for drivers to serve cross regionally

1. Total Drivers (Rural) - 78 Drivers
2. Total Drivers (Suburban) - 490 Drivers
3. Total Drivers (Urban) - 2,405 Drivers

Drivers may be isolated to serving markets regionally, over restriction may curtail supply where drivers seek to provide their services only in regions which they deem to be most beneficial.

If drivers can provide rides across adjoining regions, we will be able to fix the issue of oversupply in some regions and under supply in others, as drivers will have more flexibility to offer their services.

#### Incentivize drivers to serve rural and suburban markets

1. Average Fare (Rural) - Per Driver is $USD 55.49
2. Average Fare (Suburban) - Per Driver is $USD 39.50
3. Average Fare (Urban) - Per Driver is $USD 16.57

There are significant differences seen across average ride fare by city type. A Rural Driver on average earns upwards of 3 times that of an Urban Driver. The higher earning potential may be a useful tool to entice drivers to earn more money by providing incentives to serve their adjoining Rural and Suburban cities. This will enable us to remove the surplus supply in Urban city type and simultaneously reduce the average costs of using Ride Share services in Rural and Suburban city types improving the demand for Ride Sharing Services. 

