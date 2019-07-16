# Honolulu Climate Analysis

## Objective:
Use Python and SQLAlchemy to do basic climate analysis and data exploration of sqlite files. Analysis completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.

## Tools Used:
SQLAlchemy
ORM queries
Pandas
Matplotlib

## Steps:
 1. Import hawaii.sqlite files to explore for climate analysis and data exploration. Pick date range of two weeks.
 2. Use SQLAlchemy create_engine to connect to the sqlite database.
 3. Use SQLAlchemy automap_base() to reflect tables into classes/save a reference to those classes called Station and Measurement.
 4. Design a query to retrieve the last 12 months of precipitation data to explore rainfall trends.
 5. Design a query to calculate the total number of stations.
 6. Design a query to find the most active stations.
 7. Design a query to retrieve the last 12 months of temperature observation data (tobs).
 8. Use Pandas and MatPlotLib to visualize data pulled from queries. 

## Results:
### Precipitation Analysis
[Precipitation analysis.png]

 * Designed a query to retrieve the last 12 months of precipitation data. Selecting only the date and prcp values.
 * Load the query results into a Pandas DataFrame and set the index to the date column.
Sort the DataFrame values by date.
Plot the results using the DataFrame plot method.

### Station Analysis
[Station Analysis.png]


Design a query to calculate the total number of stations.

Design a query to find the most active stations.

List the stations and observation counts in descending order.
Which station has the highest number of observations?
Hint: You may need to use functions such as func.min, func.max, func.avg, and func.count in your queries.


### Temperature Analysis
[Temperature analysis.png]


The starter notebook contains a function called calc_temps that will accept a start date and end date in the format %Y-%m-%d and return the minimum, average, and maximum temperatures for that range of dates.
Use the calc_temps function to calculate the min, avg, and max temperatures for your trip using the matching dates from the previous year (i.e., use "2017-01-01" if your trip start date was "2018-01-01").

Plot the min, avg, and max temperature from your previous query as a bar chart.


Use the average temperature as the bar height.
Use the peak-to-peak (tmax-tmin) value as the y error bar (yerr).







Other Recommended Analysis (Optional)



The following are optional challenge queries. These are highly recommended to attempt, but not required for the homework.


Calculate the rainfall per weather station using the previous year's matching dates.



Calculate the daily normals. Normals are the averages for the min, avg, and max temperatures.


You are provided with a function called daily_normals that will calculate the daily normals for a specific date. This date string will be in the format %m-%d. Be sure to use all historic tobs that match that date string.
Create a list of dates for your trip in the format %m-%d. Use the daily_normals function to calculate the normals for each date string and append the results to a list.
Load the list of daily normals into a Pandas DataFrame and set the index equal to the date.
Use Pandas to plot an area plot (stacked=False) for the daily normals.


