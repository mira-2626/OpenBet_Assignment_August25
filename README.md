# OpenBet_Assignment_August25

Assessment project for Openbet - Data Engineer position


Prerequisites 
  1. Create a Free Databricks Workspace (if needed)
      Go to https://databricks.com/try-databricks and sign up for Databricks Community Edition (free).
  2. Create a Unity Catalog Schema
       Log in to your Databricks workspace.
       Open the Data Explorer
       Create a new schema for the assignment data called <openbet>
  3. Create Managed Volumes to Store Raw Files
        Navigate to Data Ingestion> Upload files to volume
        Create the Volume <time_management_master_data> within the Unity Catalog schema <openbet> from step 2
        Upload all master data CSV files
        Create the Volume <time_management_operational_data> within the Unity Catalog schema <openbet> from step 2
        Upload all operational data CSV files with a date extension of the form <_DDMMYYY>
  
  Overall the setup should like the below:
  
<img width="1839" height="700" alt="image" src="https://github.com/user-attachments/assets/a3a9c3c6-b894-4fe7-9e36-748f115c9643" />

     
Initial Setup
    Open your Databricks workspace
    Navigate to Workspace > Users > <your_email>
    Click Import > GitHub
    Enter the repository URL
    You wil be required to authenticate which should be a straight-forward process


Project Structure

    OpenBet_Assignment_August25/          # Project root
    ├── config/                          # Configuration files
    │   └── config.yaml                  # Paths, schemas, parameters, filenames, etc.
    ├── utils/                          # Utility/helper Python scripts
    │   └── utils.py                    # Config loader, validation, helper functions
    ├── src/                            # Source code for ingestion, processing, and queries
    │   ├── ingestion/                  # Data ingestion pipelines
    │   │   ├── master_data/            # Master data ingestion scripts/notebooks
    │   │   │   └── ingest_master_data.py
    │   │   └── daily_ingestion/        # Operational data ingestion scripts/notebooks
    │   │       └── daily_ingest.py
    
    │   ├── business_intelligence/      # Analytical queries and reporting notebooks/scripts
    │   │   └── business_intelligence.py# SQL queries for business questions
    │   └── orchestration/              # Pipeline orchestrators and job runners
    │       └── run_pipeline.py         # Runs ingestion, validation, and analytics end-to-end
    ├── tests/                         # Unit or integration tests (if applicable)
    │   └── test_ingestion.py           # Tests for ingestion code and validation
    ├── README.md                      # Project overview and instructions

Program execution

1.Run Master Data Ingestion

              Open the notebook or script for master data ingestion:
              /src/ingestion/master_data/ingest_master_data.py

2.Run Operational Data Ingestion

              Open the daily ingestion notebook/script:
              /src/ingestion/daily_ingestion/daily_ingest.py
              Set the run_date parameter (e.g., as a notebook widget or variable) to specify which day’s operational files to process.

3.Run Analytical Queries

              Open the analytics notebook business_intelligence/business_intelligence.py


Screenshots of Part B

QUESTION 1

<img width="875" height="710" alt="unbillable" src="https://github.com/user-attachments/assets/10a579d1-6a9a-4ee6-ba61-fe14d322fdf6" />

QUESTION 2

<img width="1221" height="791" alt="YEAR-TO-DATE" src="https://github.com/user-attachments/assets/2de9b5e8-f889-44ae-81c1-de95941cf705" />




Backlog

        - Address TODO: comments
        - Write Unit tests
        - Write an onchestrator
        - Create a framework to productionise the whole project
        - Schema Validation & Data Quality enhancements
        - Retry Mechanisms

License

    This project is licensed under the MIT License.


