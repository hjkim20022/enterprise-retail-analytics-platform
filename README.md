# enterprise-retail-analytics-platform
End-to-end Retail Analytics Platform using Azure Data Factory, Microsoft Fabric, PySpark, Medallion Architecture, and Power BI.

# Enterprise Retail Analytics Platform

End-to-end Retail Analytics Platform built using Azure Data Factory, Azure Blob Storage, Microsoft Fabric, Lakehouse, PySpark, Medallion Architecture, Semantic Model, and Power BI.

## Project Overview

This project demonstrates a production-style retail analytics platform that ingests multiple retail datasets using Azure Data Factory, transforms the data using Microsoft Fabric notebooks, implements the Medallion Architecture (Bronze → Silver → Gold), and delivers executive business insights through an interactive Power BI dashboard.

## Solution Architecture

```
Retail CSV Files
        │
        ▼
Azure Blob Storage (Landing)
        │
        ▼
Azure Data Factory
(Lookup + ForEach + Copy Data)
        │
        ▼
Azure Blob Storage (Bronze)
        │
        ▼
Microsoft Fabric Lakehouse
        │
        ▼
Bronze Delta Tables
        │
        ▼
Silver Layer (PySpark Transformations)
        │
        ▼
Gold Layer (Business KPIs)
        │
        ▼
Semantic Model
        │
        ▼
Power BI Executive Dashboard
        │
        ▼
Business Users
```

### Architecture Diagram

![Architecture](architecture/retail_analytics_architecture.png)

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
