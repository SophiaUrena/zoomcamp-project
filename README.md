# New York City Crimes Analytics
This project applies data engineering concepts and skills learned throughout the [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) by [DataTalksClub](https://datatalks.club/).

Crimes have a wide-ranging effects on individuals and communities as a whole, this results in a negative impact on the well-being of individuals within a community. Prevention and awareness increases by analsying the trends of crimes, which then help reduce the impact of crimes on society by creating a safer community.

The goal of this project was to develope a workflow to extracts, transforms, and loads data. This workflow will allow users to analyse crime data from New York City through a dashboard.

# Dataset
This project used the [NYPD Compliant Data Historic](https://data.cityofnewyork.us/Public-Safety/NYC-crime/qb7u-rbmr) dataset, data can be downloaded as a CSV through their website. The JSON format of this data set was used for this project and can be found here: [Link](https://drive.google.com/file/d/1lJBE-u9cbv6yowtLAeNc3Ovy5WmgY_Hs/view?usp=sharing). The dataset was updated quarterly and includes crimes reported throughout New York City.

Each complaint has an ID, description of the crime committed, along with documentation of the date and location of the occurrence. 

# Tools
Cloud - AWS S3 Bucket and Azure

Data Lake - Azure Data Lake

Data Warehouse - SQL Database

ETL - Databricks and Azure Data Factory

Data Visualization - Power BI

# Architecture
![image](https://user-images.githubusercontent.com/121827505/230258864-063b5552-42b8-4840-b4eb-d2e88cdab6b4.png)

# Steps to Reproduction
1. JSON files are placed into the AWS S3 bucket which was then copied into a Landing folder in Azure DataLake Storage Account Container using Azure Data Factory Copy Pipeline
2. The JSON files are placed into the landing folder which was then transfered into Databricks which then transfered the JSON files to a CSV file format. 
3. Another Azure Data Factory Copy Pipeline was used to extract files from the staging folder and load the files into Azure SQL Database.
4. The CSV files are then uploaded to PowerBI from the Azure SQL Database.

The setup and code for each step are included within this repository. Azure was the main cloud platform used throughout this project.

# Dashboard
![image](https://user-images.githubusercontent.com/121827505/230258778-46dce08d-ed7b-489e-933a-70aebcc6d8f4.png)

Dashboard can be viewed at this [Link](https://app.powerbi.com/links/tWmtuFf7vK?ctid=8dbcff76-671a-4b08-a48d-9d725008c017&pbi_source=linkShare).