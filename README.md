# SBDL
**Project Background **
You have a MDM platform which maintain a gold copy of all the entities and facilities within the organisation. We already have data collection and management system in place. MDM system were exposed by  some APIs for reading the most updated copy of the desired entity. This set up get complex when the number of downstream applications increases .  For scaling purpose   it would be better to  implemented kafka system to collect entity data from MDM  and letting down stream applications to read data from kafka topics . 

**Project Assumption**

It is assumed that  there is an already existing data ingestion pipeline from MDM platform to Hadoop cluster in hive table as daily partitions .


**Project Requirements**

This project focuses on extracting  data from hive table, process and prepare according to the requirements and push it to Kafka

It involves using PySpark, Sql, Databricks	


1.Entity data is available in the hive tables. The data ingestion pipeline is already in place.
2.The project focuses on developing a spark application that does the following
	1.Take load data as input argument.
	2.Read entity data from hive tables for the given load date.
	3.Process and prepare the data according to the 		  requirements.
	4.Send the prepared entity to Kafka topic.
3.Setup CI/CD pipeline

For sake of demonstration, I will be considering Accounts entity, which contains 3 tables: Accounts, Parties, Party Address
