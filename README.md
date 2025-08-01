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

    git clone <repo_url>
    cd OpenBet_Assignment_August25
