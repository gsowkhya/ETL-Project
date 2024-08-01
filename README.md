In this project, we will construct a batch ETL pipeline to extract transactional data from an RDS, transform it, and load it into target dimensions and facts in a Redshift Data Mart.

After loading the data into Redshift, we will write the specified analytical queries.

The dataset includes transactions from over 100 ATMs across Denmark, capturing details such as card type, location, date, time, and ATM type. Additionally, a transaction amount field, generated using a random function, has been included for analysis purposes.

Spar Nord Bank has developed a dimensional model datastore (ATM Data Mart) to analyze ATM usage patterns. The target schema of this Data Mart will be provided and used to create tables in Redshift.

The main tasks are as follows:
  1) Extract transactional data from a MySQL RDS server to an HDFS (EC2) instance using Sqoop.
  2) Transform the transactional data according to the provided target schema using PySpark.
  3) Load the transformed data into an S3 bucket.
  4) Create Redshift tables based on the given schema.
  5) Load the data from Amazon S3 into the Redshift tables.

Performing the following analysis queries:
  1) Top 10 ATMs where most transactions are in the ’inactive’ state
  2) Number of ATM failures corresponding to the different weather conditions recorded at the time of the transactions
  3) Top 10 ATMs with the most number of transactions throughout the year
  4) Number of overall ATM transactions going inactive per month for each month
  5) Top 10 ATMs with the highest total amount withdrawn throughout the year
  6) Number of failed ATM transactions across various card types
  7) Top 10 records with the number of transactions ordered by the ATM_number, ATM_manufacturer, location, weekend_flag and then total_transaction_count, on weekdays and on weekends throughout the year
  8) Most active day in each ATMs from location "Vejgaard"
