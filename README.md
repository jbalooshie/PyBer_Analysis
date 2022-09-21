# PyBer_Analysis
This repository was created as part of a 6 month Data Analystics Bootcamp administed by George Washington University. This is the repository for the Module 5 Challenge. This challenge served as an introduction to Matplotlib and further experience with pandas. Topics covered including creating DataFrame visualizations and cleaning datasets. Final project work is in PyBer_Challenge.ipynb. 

## Overview of the analysis
The purpose of this analysis is to explain how the type of city (rural, suburban, or urban) affects the price of the fare for the ride. This relationship is important to understand because it impacts both the driver and rider. Riders prefer to pay lower fares, while drivers want to ensure they are being adequately compensated for their work. Looking at this data can help us determine if there are gaps or inconsistencies in this relationship that need to be addressed. 

### Methods
A data frame was constructed using two csv files showing the rideshare data for specific cities, and the data for individual rides. They were combined using a common detail (the name of the city) to create one unified data frame. From there, we extracted the total rides, total drivers, total fares, average ride fare, and average driver fare for each city type. Here is an example of how the total rides was extracted: 

`total_rides = pyber_data_df.groupby(["type"]).count()["ride_id"]`

From there a formatted data frame was constructed. We then took this one step forward and created another data frame that is arranged by city type and date. We used this frame to create a breakdown of the total fares based on city type and date. This was compiled into a line chart for easy analysis. 

## Results

The below table displays the total rides, drivers, and fares paid across the three city types. It also shows the average fare per ride and average fare per driver. 

![Results Summary](https://github.com/jbalooshie/PyBer_Analysis/blob/main/analysis/summary.PNG)

The chart below shows the total fares collected over a four-month period in each of the three city types. 

![Line Chart](https://github.com/jbalooshie/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary.png)

Below, we will breakdown notable takeaways across each of the six categories that were investigated. 

### Description of Differences

- The urban city type has the most total rides taken, with 1,625. This is 13 times as many as the rural city type, with 125. Suburban cities have 625 rides taken.
- The urban city type also has the most drivers, at 2405. This almost 31 times as many drivers as the rural city type, with 78. Suburban cities have 490 drivers 
- The urban city type generates the most fares at $39,854.38. This is almost 10 times as much as rural cities generate ($4,327.93), and about 1.5 times as much as suburban cities generate ($19,356.33). 
- The average fare per ride is highest in rural cities, at $34.62. Suburban cities have a cheaper average fare ($30.97), and urban cities have the cheapest fare ($24.53). 
- The average fare per driver is also highest in rural cities, at $55.59. Drivers in suburban cities earn less on average ($39.50), and urban drivers earn the least ($16.57).
- The total fare by city type (see above line chart) has one instance where there is an increase in total fare, followed by a decrease, for all 3 city types. There is an increase in the middle of February, and then a decrease at the start of March. This is the only point across the four months where there is a trend shared by all 3 city types. 

## Summary

Based on the above results, we would like to present three recommendations for the company to address disparities among the different city types. 

### Recommendations

- Limit the number of drivers in urban cities. There are 13 times as many rides taken in urban cities than in rural cities, but there are 31 times more drivers. This means fares are being spread across more drivers, resulting in a very low average fare per driver in urban cities ($16.57). 

- Advertise using rideshares as an affordable alternative for urban transportation. The average fare price in urban areas is the lowest out of the three. Individuals in rural and suburban areas might not realize that they will be paying less when they use rideshares in urban cities (versus when they use a rideshare in a rural or suburban city). Alerting users to this fact might increase usage in urban areas. 

- Investigate why fares fluctuate for urban cities from mid-February to the start of April. During this time, the total fares for urban cities fluctuates in a way not seen for other city types. This implies that from week to week there are big differences in the number of rides being taken. It is not immediately clear why that is though. Understanding this could help the company retarget its marketing efforts to ensure more consistent demand.
