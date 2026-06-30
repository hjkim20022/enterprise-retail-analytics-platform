# enterprise-retail-analytics-platform
End-to-end Retail Analytics Platform using Azure Data Factory, Microsoft Fabric, PySpark, Medallion Architecture, and Power BI.

# Enterprise Retail Analytics Platform

End-to-end retail analytics project using Azure Data Factory, Azure Blob Storage, Microsoft Fabric, PySpark, Medallion Architecture, and Power BI.

## Project Overview

This project demonstrates a metadata-driven data ingestion pipeline for a retail analytics platform. Azure Data Factory is used to orchestrate ingestion of multiple CSV files from Azure Blob Storage Landing into a Bronze container using Lookup, ForEach, Copy Data activities, and parameterized datasets.

## Architecture

Azure Blob Storage Landing  
→ Azure Data Factory  
→ Azure Blob Storage Bronze  
→ Microsoft Fabric Lakehouse  
→ Silver and Gold Tables  
→ Power BI Dashboard

## Solution Architecture

![Architecture](architecture/retail_analytics_architecture.png)

## Completed So Far

- Created Azure Resource Group, Storage Account, and Blob containers.
- Uploaded six retail CSV source files.
- Built a metadata-driven Azure Data Factory pipeline.
- Used `file_list.csv` as a control file.
- Configured Lookup activity to read all file names.
- Configured ForEach activity to loop through the file list.
- Used parameterized datasets with `@item().FileName`.
- Successfully copied all six files from Landing to Bronze.

## Technologies Used

- Azure Data Factory
- Azure Blob Storage
- Microsoft Fabric
- PySpark
- Medallion Architecture
- Power BI
- GitHub

## Dataset

The project uses six retail CSV files:

- customers.csv
- orders.csv
- order_items.csv
- products.csv
- returns.csv
- sales_targets.csv

## Azure Data Factory Pipeline

The ingestion pipeline uses:

- `Lookup_File_List`
- `ForEach_File`
- `Copy_Landing_To_Bronze`
- `DS_Landing_CSV`
- `DS_Bronze_CSV`

## Screenshots

### Pipeline Overview
![Pipeline Overview](adf/screenshots/01_pipeline_overview.png)


### Lookup Activity
![Lookup Activity](adf/screenshots/02_lookup_activity.png)


### ForEach Settings
![ForEach Settings](adf/screenshots/03_foreach_settings.png)


### Copy Source
![Copy Source](adf/screenshots/04_copy_source.png)


### Copy Sink
![Copy Sink](adf/screenshots/05_copy_sink.png)


### Pipeline Success
![Pipeline Success](adf/screenshots/06_pipeline_success.png)


## Next Phase

The next phase will extend the project into Microsoft Fabric:

- Load Bronze data into Fabric Lakehouse.
- Create Silver cleaned tables using PySpark.
- Create Gold business KPI tables.
- Build a Power BI executive dashboard.

## Resume Highlight

Built a metadata-driven Azure Data Factory ingestion pipeline using Lookup, ForEach, Copy Data, parameterized datasets, and Azure Blob Storage to automate ingestion of multiple retail datasets into a Bronze data lake layer.
