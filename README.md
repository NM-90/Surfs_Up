# Surfs_Up
SQLite

## Overview of the Statistical Analysis

The client would like to know more information about temperature trends before opening the surf shop. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.

## Results

- The mean (average)temperature in June is 74.9 degrees Fahrenheit vs the mean temperature in December is 71 degrees Fahrenheit.  

- The minimum temp in June is 64 degress Fahrenheit vs the minimum temp in December is 56 degress Fahrenheit. 

- The maximum temp in June is 85 degress Fahrenheit vs the maximum temp in December is 83 degress Fahrenheit.

June 

<img width="154" alt="SD_June" src="https://user-images.githubusercontent.com/111452227/209065207-c6c97bc3-5afb-4301-a8c2-316955533f98.png"> 

December

<img width="146" alt="SD_Dec" src="https://user-images.githubusercontent.com/111452227/209065236-9b04d53c-ed5a-4459-ac47-0c5bac14be98.png">



## Summary

The data provided gives a better insight on whether a surf and ice cream shop business would be sustainable year-round in Oahu.  Taking a closer look at the lower 25th percentile temperature in December is 69 degrees Fahrenheit, shows us that the December temperatures are still warm enough for a scoop of ice cream or a day out surfing. The data is promising so far!  And the temperatures in June do not normally drop below 73 degrees. 

We could also look at the precipitation patters for the month of June and December buy running the following queries:

results_prec_June = session.query(Measurement.date,Measurement.prcp).filter(extract('month', Measurement.date)==6).all()
print(results)

results_prec_Dec = session.query(Measurement.date,Measurement.prcp).filter(extract('month', Measurement.date)==12).all()
print(results)



