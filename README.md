# Logistics
**Problem Statements:**

Using this dataset, the firm wants to find opportunities to improve efficiency in operations and understand how the estimated delivery time/distance varies with respect to the actual delivery time/distance.

## Concept Used:
Data Cleaning and Feature Extraction
Exploratory Data Analysis
Hypothesis Testing and Visual Analysis 
  Actual Time and Predicted Time of Trip
  Actual Time of Trip and Segment of Trip
  Predicted Distance of Trip and Segment of Trip
  Predicted Time of Trip and Segment of Trip
one-hot encoding of categorical variables (like route_type)
Column Standardization


**Insights:**
Inter and Intra State Flow of Deliveries between Top States 
  ![Flow of Delieries](https://github.com/jdeepanshu/logistics/assets/6391462/7cb2fe9a-ecef-44b0-95a4-db0a24820d81)
The majority of Delhivery's business is interstate, with Karnataka and Maharashtra being the top states.
Average Speed in Different States
  ![Average Speed in Different states](https://github.com/jdeepanshu/logistics/assets/6391462/2a5c6f42-e641-4315-a951-69ac6b09b3cc)
Delhi has the slowest speed. The interstate speed is faster than the intrastate speed. The Kerala-Karnataka interstate has a very low speed.

Trip Creation and End
  ![Number of Trips Ending by hour and day of week](https://github.com/jdeepanshu/logistics/assets/6391462/95fb3d03-d422-4519-ba15-c6cf4d40e5b4)
  ![Number of Trips created by hour and day of week](https://github.com/jdeepanshu/logistics/assets/6391462/94bd514c-c787-4599-8331-acda69434eb7)
  Trips are mostly created end of day during late hours, between 8 pm to 1 am. 
Most trips end between 5 am and 6 am, indicating higher traffic during early hours of the day. The number of trips ended is lower on Sundays and Mondays.

Inter State Cross Border Trips wrt to states
  ![Cross State with more](https://github.com/jdeepanshu/logistics/assets/6391462/943271de-2b0c-4d20-a60e-cf4aab3bb2e7)
  ![Cross State with less](https://github.com/jdeepanshu/logistics/assets/6391462/a3030bd5-abf0-4f67-99c6-9844f3832c75)
  
Delhi, Haryana, and Uttar Pradesh, which are also HQ regions of Delhivery, have the most cross-border transactions.
Karnataka, Maharashtra, Tamil Nadu, and Andhra Pradesh have fewer cross-border transactions despite having many interstate businesses.
Bengaluru/Bangalore is the busiest city with an average distance of 32 kms and an average time of 1.5 hrs.

Visual Analysis of Actual Time and Predicted OSRM Time    
  ![Distribution of Acutal and OSRM TIme](https://github.com/jdeepanshu/logistics/assets/6391462/0c2adef0-bf26-4825-879a-18438d9217cb)
Visual Analysis of Predicted Distance of Full Trip and Estimated Distance in each segment of Delivery  
  ![Distribution of OSRM Distance and Segment OSRM Distance](https://github.com/jdeepanshu/logistics/assets/6391462/871532ae-ff49-487a-9622-45edfeb70294)

On average, there is no difference between the actual time and the segment actual time.
Generally, the value of osrm distance,time is lower than that of aggregated segment values.
On the whole, actual time is higher than osrm time. Actual time extends up to 13 hours which is double the maximum osrm_time.

The Carting Trips/Full Truck Trip ratio is 2x, which can be increased further to improve short-duration deliveries for distance upto 100kms.

**Recommendations**
Improve Interstate corridors in southern India for higher-value business.
Use practices from Northern States like Haryana, Uttar Pradesh, Delhi to improve inter state business in states of Karnataka, Andhra Pradesh and Telangana.
On average, actual time exceeds OSRM time for all trips, the company should either enhance the accuracy of their forecasts or investigate the underlying reasons for delivery delays.
Considering that there are fewer trips ending on Sundays and Mondays, the company can strategize incentives or discounts to stimulate business optimization on these days.
