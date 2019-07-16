# Honolulu Climate Analysis

## Objective:
Use Python and SQLAlchemy to do basic climate analysis and data exploration of sqlite files. Analysis completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.

## Tools Used:
SQLAlchemy
FLASK
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
 9. Design a Flask API based on the previously developed queries.

## How to Run:
 ### Data Cleaning
 1. Download or clone this repository.
 2. cd into the repo folder and run jupyter notebook with terminal
```
$ cd Honolulu-Climate-Data-SQLite-Retrieval
$ jupyter notebook
```
 3. Once the notebook opens, open the climate_checker.ipynb file.

 ### Climate App
 1. run 'app.py'
 ```
$ cd Honolulu-Climate-Data-SQLite-Retrieval
$ python3 app.py
```
 2. visit [http://localhost/5000](http://localhost/5000) on your browser


## Results:
### Precipitation Analysis
![Precipitation analysis.png](https://github.com/SamLingle/Honolulu-Climate-Data-SQLite-Retrieval/blob/master/data_exploration_png_files/Precipitation_Chart.png)

![Precipitation_code](https://github.com/SamLingle/Honolulu-Climate-Data-SQLite-Retrieval/blob/master/data_exploration_png_files/Precipitation_query.png)

 * Designed a query to retrieve the last 12 months of precipitation data. Selecting only the date and prcp values.
 * Load the query results into a Pandas DataFrame and set the index to the date column.
Sort the DataFrame values by date.
Plot the results using the DataFrame plot method.

### Station Analysis
![Station Analysis.png](https://github.com/SamLingle/Honolulu-Climate-Data-SQLite-Retrieval/blob/master/data_exploration_png_files/Temperature_Analysis_chart.png)


Design a query to calculate the total number of stations.

Design a query to find the most active stations.

List the stations and observation counts in descending order.
Which station has the highest number of observations?
Hint: You may need to use functions such as func.min, func.max, func.avg, and func.count in your queries.


### Temperature Analysis
![Temperature analysis.png](https://github.com/SamLingle/Honolulu-Climate-Data-SQLite-Retrieval/blob/master/data_exploration_png_files/Average_vacation_temp.png)


The starter notebook contains a function called calc_temps that will accept a start date and end date in the format %Y-%m-%d and return the minimum, average, and maximum temperatures for that range of dates.
Use the calc_temps function to calculate the min, avg, and max temperatures for your trip using the matching dates from the previous year (i.e., use "2017-01-01" if your trip start date was "2018-01-01").

Plot the min, avg, and max temperature from your previous query as a bar chart.


Use the average temperature as the bar height.
Use the peak-to-peak (tmax-tmin) value as the y error bar (yerr).

