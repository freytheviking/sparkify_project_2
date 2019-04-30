# Project 2 - Data Modeling with Apache Cassandra

## Introduction

The purpose of this project is to help a music streaming startup called Sparkify better understand their users' listening habits. Sparkify's user base has been growing exponentially, and needs a database and analytics solution that will be able to scale and keep up with its rapid growth. We will be using Apache Cassandra, a NOSQL database, to power Sparkify's back-end and at the same time, use it to derive meaningful insights for the analytics team. 


## The Raw Data

The raw data logs come in the form of CSV files, containing records of song plays. Below is the schema of the CSV log file, named `event_datafile_new.csv`:

|column_name|description|data_type|
|:-:|---|---|
|artist|Name of the artist|text|
|firsName|First name of user|text|
|gender|Gender of user|text|
|itemInSession|Item number in session|int|
|lastName|Last name of user|text|
|length|Length of song|float|
|level|Membership level of user|text|
|location|Geographic location of user|text|
|sessionId|The session id|int|
|song|Name of song|text|
|userId|The user id|int|


## Database Design

Because there are no join in Apache Cassandra, denormalization of tables is a requirement. Practically, this means that one must understand the queries that will be run BEFORE any data modeling with Cassandra can even begin.

The questions in the form of queries that the Sparkify analytics team want to answer are:

1) `Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4`
2) `Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182`
3) `Give me every user name (first and last) in my music app history who listened to the song "All Hands Against His Own"`

Therefore, we will create one table for each of the above queries.

## Misc Architectural and Design Records


## How to Run ETL


## Example Queries
