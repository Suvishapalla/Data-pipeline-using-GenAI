# Data Pipeline Using GenAI

## Overview
This project implements an automated data pipeline using AWS and Generative AI (GPT-4).  
It performs data profiling, aggregation, cleaning, metadata extraction, and quality checks to prepare datasets for downstream analytics or machine learning.

## Project Structure
- **DataProfiling.py** – Profiles datasets for structure and statistics.  
- **Data_Aggregation.py** – Aggregates and combines multiple datasets.  
- **Data_Cleaning.py** – Cleans data (duplicates, missing values, anomalies) and stores results in S3.  
- **MetaData.py** – Extracts and stores metadata into AWS RDS; sends notifications via SNS.  
- **Quality_Check.py** – Performs detailed quality checks and generates JSON reports.  
- **portfolio.csv** – Sample dataset used in the pipeline.  
- **profile.csv** – Sample dataset used in the pipeline.  
- **Data Pipeline Using GenAI.key** – Presentation slides for the project.  
- **LICENSE** – License information.  
- **README.md** – Project documentation.  

## Requirements
- Python 3.8+  
- AWS account with configured services: S3, Lambda, Step Functions, RDS, SNS  
- Packages: `boto3`, `pandas`, `requests`, `psycopg2`, `zipfile`  
- GPT-4 API access (Azure OpenAI or equivalent)  

## Usage
1. Upload raw CSV files to the configured S3 input bucket.  
2. Trigger the pipeline through AWS Lambda or Step Functions.  
3. The pipeline will:  
   - Clean data and save results to S3.  
   - Extract and store metadata in RDS.  
   - Generate quality reports in JSON format.  
4. Monitor notifications via AWS SNS.  

## Output
- **Cleaned CSV files** in S3.  
- **Metadata records** in RDS.  
- **Quality check reports** in S3.  

