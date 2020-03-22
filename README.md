## Udacity Data Engineering Nanodegree - Project 5 Data Pipelines
The purpose of this project is to extract data from Sparkify event logs and song logs using Apache Airflow

### ETL Details
- The logs are stored in S3 for both Events and Songs
- The staging tables are used to read the logs and insert it into a tables
- The code then read the staging table and transform it into the fact and dimensions table
- The songplay table is the fact table and it stores all details about the song, user id and levels, artist and duration of the song for fast reading on analytics
- The fact table (songplay) has the details needed to know about the popularity, details of users listening to certain song based on certain time period etc.
- Airflow is used to do the data copying from S3 to Redshift Cluster seamless and periodically
- Data quality during the copying and ETL process can be ensured during the DAG run

## Running the code
- Run the Airflow in your local computer
- Place the Dags file and Plugins in the respective folder
- Setup the connection to add in "aws_credentials" & "redshift" details
- Start the Airflow webserver
- Browse available DAGs in the browser (default is at localhost:8080)

### Written by Andree Wijaya