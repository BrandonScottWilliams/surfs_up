# surfs_up
## Overview of Analysis
This analysis was performed to get insight to W. Avy as to whether opening a surf shop would be a feasible investment. The analysis used weather data from surrounding weather stations to get summary statistics of the weather in Oahu from the previous year.
## Results
* Temperatures in December got lower than June by 8 degrees.
* The maority of the temperatures fell between 73 and 77 degrees in June(Between the first and third quartile). While in December, the majority of the temperatures fell between 69 and 74 degrees. 
* The standard deviation for June was approximately 3.25 degrees and 3.74 for December.
## Summary
The data suggests that the temperatures will be relatively similar in June and December. It is expected that temperatures will show more volatility in December than June  with more of a skew towards colder temperatures in December. We can get more information on the weather, like a summary of the precipitation data using 2 additional querries.

session.query(Measurement.date,Measurement.prcp).filter(extract('month', Measurement.date)==6).all()
session.query(Measurement.date,Measurement.prcp).filter(extract('month', Measurement.date)==12).all()
