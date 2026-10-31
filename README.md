# simple-aws-serverless-data-analytics
A serverless data analytics architecture built on AWS that enables CSV data ingestion, schema discovery, SQL querying, and business intelligence visualization using AWS Lambda, Amazon S3, AWS Glue, Amazon Athena, and Amazon QuickSight. I've uploaded CSV for reference


## Architecture
<img width="1073" height="599" alt="image" src="https://github.com/user-attachments/assets/97a8b4d6-084b-4231-a402-f186452a2e05" />

### AWS Glue Crawler
Automatically scans data stored in Amazon S3 to discover its structure and schema, such as column names and data types. It then creates or updates table definitions in the AWS Glue Data Catalog.

### AWS Glue Data Catalog
A centralized metadata repository that stores table schemas, data formats, and data locations.

It does not store the actual records. Instead, it helps services like Amazon Athena understand how and where to access the data.

### Amazon Athena
A serverless SQL query service that allows users to analyze data directly from Amazon S3 without managing servers or databases.

Athena uses metadata from the AWS Glue Data Catalog to understand the data structure, then reads the actual records from S3 to execute SQL queries.


## Result in Amazon Quick Sight
<img width="1682" height="675" alt="image" src="https://github.com/user-attachments/assets/ffcca29a-8b0a-40a7-894a-4fc9ffc8620f" />

