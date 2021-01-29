First Part:

In this Repo we are going Chicago_taxi_Datatset and design a data ingestion solution for a smart city platform.The aim of the platform is to help the city better understand and predict traffic patterns and toll revenues. A secondary role is to track and identify stolen vehicles. The data will be consumed by analysts and will be made available to other agencies and 3rd parties working with the city.
You will be ingesting the following data sources:
1.	Road toll data which is contained in a PostgreSQL database on infrastructure outside of your organization’s. You receive an initial extract of data followed by periodic deltas contained in zipped CSV files. The extracts are loaded into a Google Cloud Storage Bucket for which you have a service account with read-only access.
2.	Weight sensors on a toll bridge which are controlled by a partner company. The data is pushed to your solution periodically. You are allowed to arrange with the partner company how the data will be pushed to your solution and at what frequency.
3.	Weather data via the following weather service Weather API 
4.	Lists of stolen vehicles in the form of XLSX files. These will be uploaded periodically to a GCS bucket.
5.	Traffic data (mix of API and monthly aggregated traffic data on AWS S3)

Second Part:
A team assisting the City of Chicago in providing smarter services to its citizens. The goal of your current project is to help place more electric taxis in low emission zones in the city.

For this challenge we have to focus on the following sources of data:


1.	Chicago Taxi Trips public data set on BigQuery
2.	Periodic exports of taxi GPS data pushed to a Google Cloud Storage Bucket by the individual taxi companies that operate in the city.

Our solution should satisfy the following requirements:


1.	Data should be available for dashboarding and ML within a maximum of 10 minutes after arriving from a source. The faster the better.
2.	The system should be able to handle any errors during data ingestion gracefully and not break in a way that requires manual intervention to recover.
3.	The system should ingest as much of the GPS export data as possible while handling duplicate and incomplete rows.

 Below Files are vailable to us
1.	Two GPS export zip files containing data for:
a.	Two taxi companies with up to 5 taxis per company.
b.	Four days worth of data.
c.	A file for each 10 minute period between 8 am and 8 pm. Each file contains the GPS location of each taxi for each minute in the 10 minute period.

2.	Master data files providing:
 .	Census Tracts data showing which areas are low emission zones.
a.	Taxi EV list that shows which taxi medallion (taxi id) operating at a company is an electric vehicle.
Note: a `taxi id` correlates to a taxi medallion and not an identifier for a specific vehicle. A combination of a `taxi id` and a `company` will identify a vehicle.






