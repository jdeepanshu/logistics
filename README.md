# Logistics
## Problem Statements

Using this dataset, the firm wants to find opportunities to improve efficiency in operations and understand how the estimated delivery time/distance varies with respect to the actual delivery time/distance.

## Concept Used:
Data Cleaning and Feature Extraction

Exploratory Data Analysis

Hypothesis Testing and Visual Analysis 

  Actual Time and Predicted Time of Trip
  
  Actual Time of Trip and Segment of Trip
  
  Predicted Distance of Trip and Segment of Trip
  
  Predicted Time of Trip and Segment of Trip

One-hot encoding of categorical variables (like route_type)

Column Standardization

**EDA Approach**

Case Study started with fundamental analysis like describing and printing the shape of the dataset, value_counts, descriptive statistics, etc.

After every analysis, observations are written for every operation.

Handle outliers using the IQR method

Using Univariate and bivariate analysis to visualize the effect of one variable on another variable using graphs (countplot, kdeplot, etc.).

Multivariate analysis is also used to find flow of Deliveries in each state, average speed in states using Heatmaps and pySankey

Visual Analysis using Histogram Plots, Log Distribution Plots, BoxPlots, Scatterplots

Hypothesis Testing using ttest_ind, spearmanr tests on predicted, actual distance/Time of Trip/Segment

One Hot Encoding of using Target Encoding 

Used heatmap (correlation) to find the linear relationship between numerical values.

## Insights:
**Inter and Intra State Flow of Deliveries between Top States**

  ![Flow of Delieries](https://github.com/jdeepanshu/logistics/assets/6391462/7cb2fe9a-ecef-44b0-95a4-db0a24820d81)

  The majority of Delhivery's business is interstate, with Karnataka and Maharashtra being the top states.
  
**Average Speed in Different States**

  ![Average Speed in Different states](https://github.com/jdeepanshu/logistics/assets/6391462/2a5c6f42-e641-4315-a951-69ac6b09b3cc)
  
  Delhi has the slowest speed. The interstate speed is faster than the intrastate speed. The Kerala-Karnataka interstate has a very low speed.

**Trip Creation and End Time**

  ![Number of Trips Ending by hour and day of week](https://github.com/jdeepanshu/logistics/assets/6391462/95fb3d03-d422-4519-ba15-c6cf4d40e5b4)

  Trips are mostly created end of day during late hours, between 8 pm to 1 am. 
  
  ![Number of Trips created by hour and day of week](https://github.com/jdeepanshu/logistics/assets/6391462/94bd514c-c787-4599-8331-acda69434eb7)
  
  Trips are mostly created end of day during late hours, between 8 pm to 1 am. 
  
  Most trips end between 5 am and 6 am, indicating higher traffic during early hours of the day. The number of trips ended is lower on Sundays and Mondays.

**Inter State Cross Border Trips wrt to states**

  ![Cross State with more](https://github.com/jdeepanshu/logistics/assets/6391462/943271de-2b0c-4d20-a60e-cf4aab3bb2e7)
  ![Cross State with less](https://github.com/jdeepanshu/logistics/assets/6391462/a3030bd5-abf0-4f67-99c6-9844f3832c75)
  
  Delhi, Haryana, and Uttar Pradesh, which are also HQ regions of Delhivery, have the most cross-border transactions.
 
  Karnataka, Maharashtra, Tamil Nadu, and Andhra Pradesh have fewer cross-border transactions despite having many interstate businesses.
  
  Bengaluru/Bangalore is the busiest city with an average distance of 32 kms and an average time of 1.5 hrs.

**Visual Analysis of Actual Time and Predicted OSRM Time**

  ![Distribution of Acutal and OSRM TIme](https://github.com/jdeepanshu/logistics/assets/6391462/0c2adef0-bf26-4825-879a-18438d9217cb)

   On the whole, actual time is higher than osrm time. Actual time extends up to 13 hours which is double the maximum osrm_time.

  ![image](https://github.com/jdeepanshu/logistics/assets/6391462/dbf42a20-1449-4cc7-bb0c-11e38884fc93)

  On average, there is no difference between the actual time and the segment actual time.

**Visual Analysis of Predicted OSRM Distance of Full Trip and Distance in each Segment of Delivery**

  ![Distribution of OSRM Distance and Segment OSRM Distance](https://github.com/jdeepanshu/logistics/assets/6391462/871532ae-ff49-487a-9622-45edfeb70294)

  The value of osrm distance is lower than that of aggregated segment values.

**Visual Analysis of Predicted Distance and Time of Full Trip and each segment of Delivery**

  ![image](https://github.com/jdeepanshu/logistics/assets/6391462/d04c1d58-9d94-433c-afb8-9f7d9dbf5a28)

  Generally, the value of osrm time is lower than that of aggregated segment values.
  
**Trips by Route Type**

  ![image](https://github.com/jdeepanshu/logistics/assets/6391462/b3d7e3cc-234a-4f4e-b0ae-1abfa4305935)

  The Carting Trips/Full Truck Trip ratio is 2x, which can be increased further to improve short-duration deliveries for distances upto 100kms.

**Correlation Matrix**

  ![image](https://github.com/jdeepanshu/logistics/assets/6391462/39d3204a-2b21-45f2-91c0-9bac99d60ac5)

  Our Feature Delivery Count has high correlation with actual_distance_to Destination and osrm distance.
  
  Delivery Time also has high correlation with actual_distance_to Destination and osrm distance

**Standardized Distribution of Numerical Feature** 

  ![image](https://github.com/jdeepanshu/logistics/assets/6391462/02b6e470-947c-41a3-9fc2-9a8290eced27)


## Recommendations

Improve Interstate corridors in southern India for higher-value business.

Use practices from Northern States like Haryana, Uttar Pradesh, Delhi to improve inter state business in states of Karnataka, Andhra Pradesh and Telangana.

On average, actual time exceeds OSRM time for all trips, the company should either enhance the accuracy of their forecasts or investigate the underlying reasons for delivery delays.

Considering that there are fewer trips ending on Sundays and Mondays, the company can strategize incentives or discounts to stimulate business optimization on these days.
