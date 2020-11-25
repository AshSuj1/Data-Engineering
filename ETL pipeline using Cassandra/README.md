
# Project 

Create a database for a music streaming company to analyze the data they've been collecting on songs and user activity on their new music streaming app. The data currently resides in a directory of CSV files on user activity on the app.

# Files 

1. event_data: a directory of CSV files on user activity on the app
2. Cassandra.py: Python script that builds an ETL pipeline using Apache Cassandra
3. event_data_new.csv: a smaller event data csv file called event_datafile_new csv that will be used to insert data into the Apache Cassandra tables

# Queries to be run on tables

1. Give me the artist, song title and song's length in the music app history that was heard during  sessionId = 338, and itemInSession  = 4
2. Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182    
3. Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'
