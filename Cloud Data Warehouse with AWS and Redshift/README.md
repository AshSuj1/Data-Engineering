# Project

The purpose of this project is to analyse user activity on a music streaming app, the data used is stored in a direcotry of JSON logs and a directory with JSON metadata on the songs in the app. This project builds an ETL pipeline that extracts data from S3 stages them in Redshift and transforms data into a set of dimensional tables for their analytics team.

# Dataset

The first dataset is a subset of real data from the Million Song Dataset. Each file is in JSON format and contains metadata about a song and the artist of that song. The files are partitioned by the first three letters of each song's track ID. For example, here are filepaths to two files in this dataset.

# Files 

1. create_tables.py: Python script where you will create your fact and dimension tables for the star schema in Redshift
2. sql_queries.py: Python script where you will define your SQL statements, which will be imported into create_tables.py and etl.py
3. etl.py: Python script where you will load data from S3 into staging tables on Redshift and then process that data into your analytics tables on Redshift

# How to run the Python scripts

## Instructions
1. Import all the necessary libraries
2. Write the configuration of AWS Cluster, store the important parameter in some other file
3. Configuration of boto3 which is an AWS SDK for Python
4. Using the bucket, can check whether files log files and song data files are present
5. Create an IAM User Role, Assign appropriate permissions and create the Redshift Cluster
6. Get the Value of Endpoint and Role for put into main configuration file
7. Authorize Security Access Group to Default TCP/IP Address
8. Launch database connectivity configuration
9. Go to Terminal write the command "python create_tables.py" and then "etl.py"

To create the database tables and run the ETL pipeline, you must run the following two files in the order that they are listed below

To create tables:
```
python3 create_tables.py
```
To fill tables via ETL:

```
python3 etl.py
```

