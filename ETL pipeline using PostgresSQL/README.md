# Purpose of this project

The purpose of this project is to analyse user activity on a music streaming app, the data used is stored in a direcotry of JSON logs and a directory with JSON metadata on the songs in the app. The purpose of this project is to enable easier analysis of the data. To do so we must create a Relational Database Schema, and then configure an ETL process that would ultimately load the data into this schema.

# Files 
1. data: Folder containing JSON files of songs and log data
2. create_tables.py: Python script to perform SQL-Statements for (re-)creating database and tables
3. sql_queries.py: Python script containing SQL-Statements used by create_tables.py and etl.py
4. etl.py: Python script to extract the needed information from Song and Log data inside the data folder and parsing/inserting them to the created database schema and tables
5. test.ipynb: Displays the first few rows of each table to let you check your database

# Purpose of this database

The purpose of this database is to more easily perform queries, the ability to do joins, write complex queries and aggregations. The database also allows for the use of ad-hoc queries.


# The database schema design and ETL pipeline.

The star schema allows for faster query performance, with the fact table containing information on each song played on the music streaming app and other information pertaining to that song-play from the dimension tables such as user id and location of the user. In other words the Star schema provides an easier mechanism to query User behavior.

The ETL pipeline is neccessary to:

- extract all the relevant metadata on the songs available on the music streaming 
- extract the data that is significant to understanding user behavior from the log files 
- transform the data such as data in the time table
- load this data into the schema for easy analysis

# How to run the Python scripts

1. Run create_tables.py to create the tables
2. Run etl.py to insert relevant data into tables





