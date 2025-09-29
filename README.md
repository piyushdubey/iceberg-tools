# iceberg-tools
Simple utilities for experimenting with Apache Iceberg deletes.

## Prerequisites
Install Docker Desktop

## Steps to run the util
1. Clone this repo
2. Verify that docker is installed correctly. Run `docker -v`
3. Navigate to the newly cloned repo and run `docker-compose up`
4. Navigate to `http://localhost:8888/` > `notebooks` > `spark-warehouse` > `iceberg_deletion_experiments_notebook.ipynb`
5. Run the Notebook. (There are three different delete cells that individually delete the rows with `write.delete.granularity = file`)
6. This will generate the Position Deletes.
7. To view the Position Delete files go to `http://localhost:9001`.
   - Login with username `admin` and password `password`
   - Navigate to `warehouse` > `<database-name` (in this case `nyc`) > `<table-name>` (in this case `taxis`) to view the table
8.  To inspect the position deletes get `parquet-tools` locally or go to https://dataconverter.io/view/parquet
