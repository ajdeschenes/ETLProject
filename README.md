# Proximity of Reported Crimes to Police Stations in Chicago

This database is sourced from data published by the [City of Chicago](https://data.cityofchicago.org "City of Chicago | Data Portal")

Extraction
-------
The API urls provided by the City of Chicago were used to return raw JSON data, which we converted into Pandas DataFrames for reported crimes and police stations. 

Transformation
------
The latitude and longitude were rounded to the first decimal place and those values concatenated in order to form a primary key on which those tables could be merged. After dropping the NA values and extra columns, the remaining columns were renamed. 

Loading
------
With SQLAlchemy, we created a MySQL database and table to hold the resulting DataFrame locally. 
