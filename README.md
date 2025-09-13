# Yellow-taxi-trip-analysis-using-Hive


•	You can also get the complete data online through this link - https://data.cityofnewyork.us/Transportation/2018-Yellow-Taxi-Trip-Data/t29m-gskq
•	The data dictionary is also available and you can refer to the attached document.
Tasks related to taxi data:

1.	Create a table named taxidata . Required ddl script is given below.
CREATE TABLE IF NOT EXISTS taxidata
(vendor_id string, pickup_datetime string,
dropoff_datetime string, passenger_count int, trip_distance DECIMAL(9,6),
pickup_longitude DECIMAL(9,6), pickup_latitude DECIMAL(9,6), rate_code int,
store_and_fwd_flag string, dropoff_longitude DECIMAL(9,6), dropoff_latitude
DECIMAL(9,6),
payment_type string, fare_amount DECIMAL(9,6), extra DECIMAL(9,6),
mta_tax DECIMAL(9,6), tip_amount DECIMAL(9,6), tolls_amount DECIMAL(9,6),
total_amount DECIMAL(9,6), trip_time_in_secs int )
ROW FORMAT DELIMITED FIELDS TERMINATED BY ',' STORED as TEXTFILE
TBLPROPERTIES ("skip.header.line.count"="1")

2.	Load data from the csv file - 2018_Yellow_Taxi_Trip_Data..csv

3.	Run some basic queries to check the data is loaded properly
