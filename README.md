# spotify-end-to-end-data-engineering-project

### Introduction

In this project we will be creating an ETL(Extract, Transform, Load) pipeline using Spotify API on AWS. The pipeline will retrieve data from Spotify API, transform it into desired format and load it into an AWS data store.

### Architecture
![Architecture diagram](https://github.com/NishitaJoshi21/spotify-end-to-end-data-engineering-project/blob/main/Pipeline%20architecture.png
)

### API / Dataset Used

**Spotify Web API** – The project uses the official Spotify Web API to fetch real-time music data such as recently played tracks, artist details, and track metadata.
The API documentation provides endpoints for authentication, retrieving user activity, and accessing Spotify’s rich catalog of music data, making it ideal for building automated data pipelines.

### Services Used
1. **Amazon S3** – Used as the central data lake for storing raw and processed Spotify datasets in a scalable and cost-effective way.

2. **AWS Lambda** – Serverless functions that automate data extraction, transformation, and loading (ETL) without managing any servers.

3. **Amazon CloudWatch** – Handles monitoring and logging of Lambda executions to ensure smooth pipeline runs and quick debugging.

4. **AWS Glue Crawler** – Automatically scans data stored in S3 and updates table schemas without manual intervention.

5. **AWS Glue Data Catalog** – Acts as a unified metadata repository that stores table definitions and makes data query-ready.

6. **Amazon Athena** – A serverless query engine used to run SQL queries directly on S3 data for analysis and reporting.

### Project Execution Flow
Extract data from API -> Lambda Trigger(every 1 hr) -> Run extract code -> Store raw data -> Trigger Tranform function -> Tranform Data and Load it -> Quering using athena 

