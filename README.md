# PyBer_Analysis

## Overview of the Analysis 
The purpose of this new analysis is to perform exploratory analysis on large data files with multiple forms of data visualizaton using Matplotlib, pandas libraries, and jupyter notebook that shows the correlation between cities and number of writers along with total fares, riders, and drivers by type of cities. This analysis and visualization will help determine trends in access and affortabilty to project for certain neigborhoods. Below is the deliverables of a summary DataFrame of the ride-sharing data by city type and a multiple-line graph that shows the total weekly fares for each city type for this analysis. 

## Results 
### 1. Produce Summary Dataframe
A summary dataframe was produced by the following code: 

- Get the total rides for each city type

`total_rides_city_type = pyber_data_df.groupby(["type"]).count()["ride_id"]
total_rides_city_type`

- Get the total drivers for each city type

`total_drivers_city_type = city_data_df.groupby(["type"]).sum()["driver_count"]
total_drivers_city_type`

- Get the total amount of fares for each city type

`total_fares_city_type = pyber_data_df.groupby(["type"]).sum()["fare"]
total_fares_city_type`

- Get the average fare per ride for each city type.  

`avg_fare_per_ride_city_type = total_fares_city_type / total_rides_city_type
avg_fare_per_ride_city_type`

- Get the average fare per driver for each city type. 

`avg_fare_per_driver_city_type = total_fares_city_type / total_drivers_city_type
avg_fare_per_driver_city_type`

- The following summary dataframe was the output from the code above: 
