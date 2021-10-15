

Data Warehouse Project


With this project data has been loading for user and song databases of Sparkify to AWS cloud servises. The original data is located ASW S3 services. With the ETL process we build, we will move this data to staging tables first and then using this staging tables to final tables in AWS Redhift.


There are 3 buckets of data in AWS S3 services. They are described as below.

LOG_DATA='s3://udacity-dend/log_data'
LOG_JSONPATH='s3://udacity-dend/log_json_path.json'
SONG_DATA='s3://udacity-dend/song_data'

Star schema optimized for queries on song play analysis. This includes the following tables.

Fact Table
    songplays		

Dimension Tables
    users
    artists
    time
    songs

Data Warehouse Setup

I have created a IAM user in AWS account. Using the secret key and access key we created S3 and Redshift clients. After that, I have created a redshift cluster and completed the dwh.cfg file with the necessary credentials

Execution of the Project

I have first run the create_tables on terminal. It will use the SQL statements we created in sql_queries.py file. Then finally run the etl.py file to fill the tables which created with the source data.

