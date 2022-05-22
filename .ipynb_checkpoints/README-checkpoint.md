# Creating an OLAP database from Sparkify's music streaming app data

### Summary
This is small data engineering project whose purpose is to create an OLAP database for analyzing data on songs and user activities from Sparkify's music streaming app. The resulting database will follow the star schema design, where the fact table contains historical data about song plays, and the dimension tables contain data for songs, artists, listening users and time.

### Files
`data` - This folder contains JSON files used for creating the analytical database, they are separated into two folders: `loc_data` and `song_data`.
`sql_queries.py` - This Python script contains all SQL queries that will be used for creating the database.
`create_tables.py` - This Python script will execute SQL queries from `sql_queries.py` to create the database and the tables.
`etl.py` - This Python script will read files from `data`, process them, and execute SQL queries from `sql_queries.py` to populate data in the database.
`etl.ipynb` - This notebook is used to implement and test ETL logics. Once it's done, those logics will be implemented in `etl.py`.
`test.ipynb` - This notebook is used to check if the database and the tables were created successfully, the data types and contrains are valid and the inserted data are correctly processed.

### How to run
Prerequisite: Python 3 and Jupyter Notebook is installed.
- Open a terminal (or a Command Prompt for Windows) and navigate to the project folder.
- Run the command `python create_tables.py` to create the database **sparkifydb** and the tables.
- Run the command `python etl.py` to populate data in the database.
- Run the command `jupyter-notebook test.ipynb` to open the notebook and run cells to check if the database is correctly created and populated.
