# iceberg-tools
Iceberg Tools

# Prerequisites
Install Docker Desktop

# Steps to run the utility
1. Clone this repo
2. Navigate to `http://localhost:8888/` > `notebooks` > `spark-warehouse` > `iceberg_deletion_experiments_notebook.ipynb`
3. Run the Notebook. (There are three different delete cells that individually delete the rows with `write.delete.granularity = file`)
4. This will generate the Position Deletes.
5. To view the Position Delete files go to `http://localhost:9001`.
  3.1 Login with username `admin` and password `password`
  3.2 Navigate to `warehouse` > `<database-name` (in this case `nyc`) > `<table-name>` (in this case `taxis`) to view the table
6.  To inspect the position deletes get `parquet-tools` locally or go to https://dataconverter.io/view/parquet
