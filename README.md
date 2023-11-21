# Project 4: Predicting Flight Delays


## Table of Contents

1. [Introduction](#introduction)
2. [Data Processing](#data-processing)
3. [Initial Assessment](#initial-assessment)
4. [Delay Observations](#delay-observations)
5. [Predictions: Logical Regression & Random Forest](#predictions-logical-regression-&-random-forest)
6. [Conclusion](#conclusion)
7. [Summary & Next Steps](#summary-&-next-steps)
8. [References](#references)


## Introduction
The holidays are approaching and many are beginning to consider travel plans. Considering the delays one may face, is it worth it?

Though there are many inconveniences travellers may encounter, I chose to focus on delays. Cancellations, for example, typically stem from extreme circumstances such as weather or threat- if one flight is canceled, likely multiple or all will follow suit regardless of the flight path or airlines.

According to the FAA, a flight is considered delayed if it has not taken off within 15 minutes of its scheduled departure time.

Common causes of delays include:
- Security 
- Weather
- Late arriving aircraft

Delays result in a wide-range of negative effects for carriers, passengers, and beyond. Is it possible to predict if a flight will be delayed?


## Data Processing
I obtained my dataset from the Bureau of Transport Statistics and evaluated US flight records from September 2022 - August 2023. 

Processing was an arduous process as my combined set contained nearly 6.8 million records. In addition to dropping NAN entries and columns that didn't offer value, I eliminated additional columns that could result in a dummy variable trap. This could have given a particular dimension an unintended advantage which could affect prediction outcomes. 

While it would have been interesting to examine and predict delay reasons, the data was not consistently populated, so I dropped those columns as well. Data types were updated as needed, and select data points were remapped for ease of understanding. Finally, I did keep a full set of the processed data for my reference, but a reduced set (150001 entries) was shuffled and saved for further analysis.

Two standard prediction models were selected to test the data.
- Linear regression 
- Random Forest


## Initial Assessment
The larger cleaned dataset was loaded into Tableau for an initial analysis. The worksheets can be viewed here: https://public.tableau.com/app/profile/l.r2915/viz/PredictingFlightDelays_16999420088310/Departures_Month?publish=yes


## Delay Observations
The most delayed origins and destinations charts were topped by similar airport codes. The most delayed airlines also happen to provide the most flights. Naturally, the busiest locations and top service companies will experience a higher chance of delays.

Additional delay notes:
- Peaks in July/August, and December
- Very slight trendline decrease as month progresses
- Peaks dates 5th, 11th, 22nd – 26th
- Significant decrease in delays on 31st correlates with fewer scheduled flights
- Fewer delays observed on Tuesdays and Saturdays


## Predictions: Logical Regression & Random Forest


### Logical Regression



### Random Forest




## Conclusion


Government shutdowns, technical glitches, and other unusual events makes it difficult to consistently predict delays for a given path.

Supplementing predictions with real-time monitoring of news, dates, and weather conditions may offer the best chance of at least being prepared for a delay.



## Summary & Next Steps


### Project Constraints
Locating detailed time and reliable delay reason indicators can help further refine the model and results.

Additionally, memory issues prevented me from processing a proper representative sample.

### Future Prospects
Applying additional technologies can make the model more robust and interactive
- User interface for path lookup
- Weather forecasting and mapping for the date and path of the flight


## References
- Office Hours & Class Exercises
- Bureau of Transportation Statistics
- https://www.npr.org/2023/11/09/1211064462/southwest-airlines-flight-cancellations-holiday-travel 
- https://en.wikipedia.org/wiki/Flight_cancellation_and_delay#:~:text=A%20flight%20delay%20occurs%20when,later%20than%20its%20scheduled%20time. 
- https://aspm.faa.gov/aspmhelp/index/Types_of_Delay.html
- https://github.com/maptv/AnomalyDetection
- https://www.w3schools.com/python/python_ml_confusion_matrix.asp
- https://www.vantage-ai.com/en/blog/4-strategies-how-to-deal-with-large-datasets-in-pandas#:~:text=Another%20way%20to%20drastically%20reduce,that%20refer%20to%20these%20strings
- https://stackoverflow.com/questions/38300152/how-to-significantly-reduce-size-of-dataset-say-csv-to-analyse-in-pandas
- https://www.learndatasci.com/glossary/dummy-variable-trap/
- https://www.geeksforgeeks.org/using-dictionary-to-remap-values-in-pandas-dataframe-columns/#
- https://stackoverflow.com/questions/29576430/shuffle-dataframe-rows
- https://towardsdatascience.com/mastering-random-forests-a-comprehensive-guide-51307c129cb1