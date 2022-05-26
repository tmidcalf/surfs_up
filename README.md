# Surf's Up
Exploring Weather Data for A Surf/Ice Cream Shop

## Overview 

We want to start a business that sells surfing gear as well as ice cream in Oahu, Hawaii. We are tasked with performing an analysis to look at the temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.

## Results

- From our analysis we found that for the 1,700 temperatures recorded for in the month of June over the last decade, we observe an average temperature of about 74.9 degrees fahrenheit.

- Also, from our analysis we found that for the 1,517 temperatures recorded for in the month of December over the last decade, we observe an average temperature of about 71.0 degrees fahrenheit.

- One more thing to note, the max for June was 85 degrees fahrenheit and the max for December was 83 degrees fahrenheit. This means we only noticed an increase of two degrees in the highest temperatures recorded in June and December.


The images below are the results we observed from our analysis

![alt text](https://github.com/tmidcalf/surfs_up/blob/main/Resources/June_Temps.png?raw=true) ![alt text](https://github.com/tmidcalf/surfs_up/blob/main/Resources/Dec_Temps.png?raw=true)

## Summary

From the results of the analysis, we can notice little variation between the temperatures in the months of June and those in December. From this, we can conclude that Oahu seems to be a great location to open a surf supply and ice cream shop.

We might also want to look at the precipitation data in those months as well as the temperature data we observed. Two more queries we might like to run could look like the following:

- The first one to find all the precipitation data for the month of June
    ```
        session.query(Measurement.date, Measurement.prcp).filter
            (extract('month', Measurement.date)==6).all()
    ```
Then after performing this query, create a dataframe from this list and print out the summary statistics for the amount of precipitation in the month of June.

- The first one to find all the precipitation data for the month of December
    ```
        session.query(Measurement.date, Measurement.prcp).filter
            (extract('month', Measurement.date)==12).all()
    ```
Then after performing this query, just like June, create a dataframe from this list and print out the summary statistics for the amount of precipitation in the month of December.

