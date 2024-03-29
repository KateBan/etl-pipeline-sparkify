# Project: Data Modeling with Postgres

## Introduction
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

So as a data engineer I should create a Postgres database with tables designed to optimize queries on song play analysis. I will create a database schema and ETL pipeline for Song Play Analysis. 


## Schema for Song Play Analysis
Using the song and log datasets, I have created a fact and dimension tables for a star schema. This includes the following tables.

### Fact Table
songplays - records in log data associated with song plays i.e. records with page NextSong
`songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent`


### Dimension Tables
users - users in the app
`user_id, first_name, last_name, gender, level`

songs - songs in music database
`song_id, title, artist_id, year, duration`

artists - artists in music database
`artist_id, name, location, lattitude, longitude`

time - timestamps of records in songplays broken down into specific units
`start_time, hour, day, week, month, year, weekday`



## Creatin the Sparkify Database
The CREATE and DROP statements for creating and droping the tables can be found in the sql_queries.py file. Running create_tables.py will create the database and tables. We can run test.ipynb to confirm the creation of the tables with the correct columns. 

## Build ETL Processes
In the etl.ipynb notebook the development of the ETL processes for each table is presented. 

## Build ETL Pipeline
To process the entire datasets the etl.py should be used. 

