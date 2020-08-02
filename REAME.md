# CIAT Project Policies Cube Model

## Configuration

Update your database connection details on the file **connection_details.csv** located on the folder **2. Pentaho ETL\db_configuration**. You should specify hostname, database name, connection port, username and password for both your transactional and DW databases.

## Deployment

* Create the tables needed for the cube, by executing the script **create_tables_script.sql** located on the folder **1. Policy cube model** on your DW database.
* Load the time dimension data, by executing the PDI Job **load_dm_time.kjb** located on the folder **2. Pentaho ETL**.
* Load the remaining dimensions and the policies fact table, by executing the PDI Job **load_policy_cube.kjb** located on the folder **2. Pentaho ETL**.
