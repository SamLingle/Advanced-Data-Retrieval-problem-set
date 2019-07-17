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

The data shows that the highest levels of rainfall occured during the spring and fall months. While the lowest levels occured during the summer months. This information fits with what I already suspected, but provides valuable insight on the best travel dates for a trip.

### Station Analysis
![Station Analysis.png](https://github.com/SamLingle/Honolulu-Climate-Data-SQLite-Retrieval/blob/master/data_exploration_png_files/Temperature_Analysis_chart.png)

 * TOBS - Temperature of Observed Station.

To remove clutter, I found the most active station and visualized the most frequently observed temperatures to take an average of the weather. The temperature seems to trend around 75 degrees fahrenheit and range between 70 - 80 degrees. This data can be used to plan what kind of clothes to bring while traveling to the island of Oahu. 


### Temperature Analysis
![Temperature analysis.png](https://github.com/SamLingle/Honolulu-Climate-Data-SQLite-Retrieval/blob/master/data_exploration_png_files/Average_vacation_temp.png)

Created a bar chart looking at the average, minimum and maximum temperatures to plan for any extreme weather that could occur. found the max temperature of about 100 degrees and a minimum of 40. Both of which are temperatures that most people living in the united states should be well aquainted with. So I don't forsee those causing any issues while traveling. 

