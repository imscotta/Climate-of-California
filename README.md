<h1>Climate of California</h1>

For our group project we are explore historical data on fires and droughts in California from the past twenty years. Our sources are CaliforniaData.gov and Drought.gov. We extracted csv files from each site and transformed the data with Python and Pandas libraries. The data consists of one file for the fire data, that lists each fire from the past twenty years along with size and dates, and another csv for drought severity on a scale of 0-100% for the past twenty years. 

We combine the data to analyze the relationships between the drought levels and the acres burned for each year.

## Process

### Extract:
* The data our project was gathered from www.californiadata.gov/ and www.drought.gov/ as CSVs. We imported the CSVs into Python and created a dataframe for each CSV using the pandas library.

### Transform:
* We filtered the dataframes to remove columns that were uniformally used from both the fire and drought dataframe. We also renamed some of the columns to be more meaningful and descriptive.
* We formatted the dates on the fire dataframe using datetime formatting so that the dates could be compared to the dates in the drought dataframe.
* We removed 4 rows from the fire dataframe because the years were invalid.
* The 2 dataframes were then merged together using SQL LEFT JOIN to discover the drought condition during each fire in the dataframe that had a corresponding date.

### Load:
* We loaded our merged dataframe into a single SQL table in PostgreSQL.
* We ensured the column names matched the columns created in our Python notebook to validate the load of the dataframe into PostgreSQL.

## Findings
* 6,432 fires occurred since 2002 burning a total of 14,869,702 acres
* 77% of the fires occured during the presence of Abdnormally Dry conditions in at least of 75% of all California.

<img align="center" src="Images/California Fires and Drought Conditions.png" width="500" />
<img align="center" src="Images/Fires Overview.png" width="500" />
