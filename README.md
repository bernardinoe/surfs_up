# Surfs Up

## Overview of the analysis: Explain the purpose of this analy
The purpose of the analysis was understand the key difference between the weather in June and December.

## Results: Provide a bulleted list with three major points from the two analysis deliverables. Use images as support where needed.

![JuneTemp](https://github.com/bernardinoe/surfs_up/blob/main/JuneTemps.PNG)
![DecemberTemp](https://github.com/bernardinoe/surfs_up/blob/main/DecemberTemps.PNG)

- There is a count of 1700 records for June and 1517 records for December
- There is an average temperature of 74.94 for June and 71.04 for December
- The minimun temperatures are 64 for June and 56 for December

## Summary: Provide a high-level summary of the results and two additional queries that you would perform to gather more weather data for June and December.

Even thought both the average temperatures and the maximu temperatures are only a few degrees apart, the difference in the minimun temperatures is bigger. 

- I would create a plot in order to vizualize the highest and lowest records and try to understand in which period they are
df.plot()

- I would also run the query per year, in order to see where does the month stands vs the entire year
results = []
results = session.query(Measurement.date, Measurement.tobs).filter(extract('year', Measurement.date)==2010).all()
print(results)