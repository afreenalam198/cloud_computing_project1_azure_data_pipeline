# Cloud Computing Project 1: End-to-end data pipeline using Azure Data Factory

This project demonstrates building an end-to-end data pipeline on Azure to extract, process, and store data from a CSV file into an Azure SQL Database.  The core component is Azure Data Factory, orchestrating the data movement and transformation.  

## Project Overview

The primary objective is to create a robust and efficient data pipeline that ingests data from a CSV file stored in Azure Blob Storage, transforms it as needed, and loads it into an Azure SQL Database.  This pipeline leverages the power of Azure Data Factory to automate and manage this process.  

## Architecture

The data pipeline follows a simple yet effective architecture:

1.  **Data Source:** CSV file (`student-dataset-1.csv`) residing in Azure Blob Storage.
2.  **Data Processing:** Azure Data Factory pipeline handles data extraction, transformation (if any), and loading.
3.  **Data Destination:** Azure SQL Database.

## Implementation Steps

1.  **Azure Setup:**
    *   Selected a suitable Azure Subscription (e.g., Free Trial).
    *   Created an Azure Storage Account.
    *   Created a Blob Container within the Storage Account.
    *   Uploaded the `student-dataset-1.csv` file to the Blob Container.
    *   Provisioned an Azure SQL Database and configured it.

2.  **Database Setup:**
    *   Connected to the Azure SQL Database using Azure Data Studio.
    *   Created the `Students` table with the appropriate schema to match the CSV data.

3.  **Data Factory Development:**
    *   Created an Azure Data Factory instance.
    *   Launched the Azure Data Factory portal.
    *   Created Linked Services to connect to both Azure Blob Storage and Azure SQL Database.
    *   Defined Datasets representing the source CSV file and the destination SQL table.
    *   Designed the pipeline using a Copy Data activity:
        *   Source: Blob Storage Dataset (pointing to the CSV file).
        *   Sink: SQL Database Dataset (pointing to the `Students` table).
    *   Tested and debugged the pipeline to ensure successful data transfer.
    *   Published the pipeline to deploy it to Azure.
    *   Verified the data transfer by querying the `Students` table in Azure Data Studio (e.g., counting students by country).

4.  **Static Web App Deployment:**
    *   Developed an Azure Static Web App to provide a user interface for interacting with the data.
    *   Created Azure Function Apps to fetch data.

## Technologies Used

*   **Core Components:**
    *   Azure Subscription
    *   Azure Storage Account (for Blob Storage)
    *   Azure SQL Database
    *   Azure Data Factory
    *   Azure Data Studio (for database interaction and querying)  
    *   Azure Static Web App (for data visualization)
    *   Azure Function App (for API integration)
