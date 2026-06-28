# Udacity Nanodegree / WGU D497 Project #2

# Sparkify PostgreSQL Data Modeling and ETL Pipeline

## Project Overview


A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

As a developer on this project, I've been asked to create a Postgres database with tables designed to optimize queries on song play analysis, and bring you on the project. My role is to create a database schema and ETL pipeline for this analysis. I will be able to test my database and ETL pipeline by running queries given to me by the analytics team from Sparkify and compare my results with their expected results.

## Files Included

1. **etl.ipynb** - This file contains the four functions for the full-scale ETL process.
2. **test.ipynb** - This file allows for checking of the database.
3. **create_tables.py** - This file holds all the functions for the (dropping of and) creation, insert, and join of our SQL tables.
4. **etl.py** - This file reads and processes from song_data and log_data and inserts that data into our tables.
5. **sql_queries** - contains all SQL queries used by the above files

## Database Schema Design (Star Schema)

To optimize retrieval of our data, I've used a Star Schema with one fact table and four dimension tables. The Star Schema was chosen to help the analysts at Sparkify run faster queries on the data.

**songplays** Records the log data asssociated with the Sparkify streaming events
**users** Contains users registered with Sparkify
**songs** Songs available for streaming on the Sparkify platform
**artists** Artists associated with songs available on Sparkify
**time** Timestamps of each record of songplays broken into parsed time sections for easier manipulation 

## How to run this Project
Using the etl.ipynb notebook, scroll to the very bottom of the notebook and execute the cell that contains the following commands:

%run create_tables.py
%run etl.py

(Note: Make sure that the kernel has been reset and that no other file is actively using the database)

## Personal Note

#### **This project was only difficult because the project could only run one file at a time. If I could open and use as a reference all the files at the same time this project would've gone much smoother. There is an ETL project I'm developing at my job from ERP, to an on-premise database and some of that data back to a different ERP and the syntax and modularity of that project is similar to the ones used here. That project uses databricks, and I find it much easier to use than to do ETL work inside of Jupyter Labs. The best tip for myself and others is to download all the necessary files and open the data externally and look at it first before trying to write anything. It's much easier when you can easily view and reference the material. I also need to get better at using Github and writing README files because in other projects I was able to make a personal mark on the notebooks themselves, but it is preferred to keep all notes inside of the README and keep only necessary notes and process information inside the notebooks and I need to get better in that regard.**