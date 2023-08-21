Part 1: Analyze and Explore the Climate Data

1.Use the create_engine() function from SQLAlchemy to connect to your SQLite database.

2.Reflect your database tables into classes using the automap_base() function and save references to the classes named station and measurement.

3.Create a SQLAlchemy session to link Python to the database. Make sure to close the session at the end.

4.Perform a precipitation analysis:

    Find the most recent date in the dataset.
    Retrieve the previous 12 months of precipitation data using a query.
    Load the query results into a Pandas DataFrame and set column names.
    Sort the DataFrame values by date.
    Plot the results using the DataFrame's plot method.
    Print summary statistics for the precipitation data.
    Perform a station analysis:

5.Design a query to calculate the total number of stations.
    Design a query to find the most-active stations by listing stations and their observation counts in descending order.
    Design a query to calculate lowest, highest, and average temperatures for the most-active station.
    Query the previous 12 months of temperature observations (TOBS) for that station.
    Plot the TOBS results as a histogram with bins=12.
Part 2: Design Your Climate App

Now that you've analyzed the data, you'll design a Flask API with the following routes:

/: Start at the homepage and list all available routes.
/api/v1.0/precipitation: Return JSON representation of precipitation data for the last 12 months.
/api/v1.0/stations: Return a JSON list of stations.
/api/v1.0/tobs: Query and return JSON list of temperature observations for the most-active station over the previous year.
/api/v1.0/<start> and /api/v1.0/<start>/<end>: Return JSON list of minimum, average, and maximum temperatures for specified date ranges.
