# sqlalchemy-challenge

# Project
Congratulations! You've decided to treat yourself to a long holiday vacation in Honolulu, Hawaii. To help with your trip planning, you decide to do a climate analysis about the area. The following sections outline the steps that you need to take to accomplish this task.

## Part 1: Analyze and Explore the Climate Data
# Precipitation Analysis
Find the most recent date in the dataset.
Using that date, get the previous 12 months of precipitation data by querying the previous 12 months of data.
Select only the "date" and "prcp" values.
Load the query results into a Pandas DataFrame, and set the index to the "date" column.
Sort the DataFrame values by "date".
Plot the results by using the DataFrame plot method, as the following image shows:
![precipitation_bar_graph](https://user-images.githubusercontent.com/115199874/208237192-8a285a87-a884-4fc3-852b-a2b894e38119.png)

# Station Analysis
1)Design a query to calculate the total number of stations in the dataset.
2)Design a query to find the most-active stations (that is, the stations that have the most rows). To do so, complete the following steps:
3)List the stations and observation counts in descending order.
4)Answer the following question: which station id has the greatest number of observations?
5)Design a query that calculates the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.
6)Design a query to get the previous 12 months of temperature observation (TOBS) data. To do so, complete the following steps:
7)Filter by the station that has the greatest number of observations.
8)Query the previous 12 months of TOBS data for that station.
9)Plot the results as a histogram with bins=12, as the following image shows:
![Temperature_hist](https://user-images.githubusercontent.com/115199874/208237204-613f2dbd-5245-4a65-92d1-47c226f6901b.png)

# Part 2: Design Your Climate App
In this part, we design a Flask API based on the previous queries, we use Flask to create the following routes:
/
Start at the homepage.
List all the available routes:
/api/v1.0/precipitation
Convert the query results from your precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value.
Return the JSON representation of your dictionary.
/api/v1.0/stations
Return a JSON list of stations from the dataset.
/api/v1.0/tobs
Query the dates and temperature observations of the most-active station for the previous year of data.
Return a JSON list of temperature observations for the previous year.
/api/v1.0/<start> and /api/v1.0/<start>/<end>
Return a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range.
For a specified start, calculate TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date.
For a specified start date and end date, calculate TMIN, TAVG, and TMAX for the dates from the start date to the end date, inclusive.

# List of ressources
Images:
-precipitation_bar_graph.png
-Temprature_hist.png

CSV files:
-hawaii_measurements.csv
-hawaii_stations.csv
