# ETL Database dvdrental using DBeaver & Pentaho

The *dvdrental* database is a relational database designed to support the operations of a DVD rental business. It provides structured data about customers, movie inventory, rental transactions, and other aspects related to managing a rental service. This database is commonly used as a case study or for practice in data management with PostgreSQL.

## Table of Contents

- [Objective](#objective)
- [Tools](#tools)
- [ER Model](#er-model)
- [Star Schema Data Warehouse](#star-schema-data-warehouse)
- [Steps](#steps)

## Objective

- Restore _dvdrental_ database on postgreSQL database system.
- Explore and create staging using SQL query through DBeaver (including log data).
- Create data warehouse design with star schema model.
- Perform ETL process to create data warehouse and data mart using Pentaho.

## Tools
- pgadmin4
- DBeaver Community
- Pentaho Data Integration (PDI)

## ER Model
<img width="495" alt="ER Diagram dvdrental" src="https://github.com/user-attachments/assets/b35ecb9c-8a35-4377-a925-7680567f2562" />

## Star Schema Data Warehouse
![star schema dvdrental](https://github.com/user-attachments/assets/10c78190-9c35-4811-8dcf-5e7c549c4e8f)

## Steps
1. Download the _dvdrental_ file (.tar) and restore the database using pgadmin4.
2. Create a staging database (includes _staging_ and _log_ schema) by taking the _dvdrental_ database DDL (use DBeaver).
3. Create a new database (e.g. dwh_dvdrental) with 3 schemas, for data warehouse (dwh), log table (log), and data mart (datamart).
4. Open Pentaho and make a database connection on all satabases (dvdrental, staging, and dwh_dvdrental).
5. Download all transformation files (.ktr) and jobs (.kjb), then import them into Pentaho.
6. Adjust the connection on all staging trsnsformations, then run the main_job.
7. After staging is formed, run the data warehouse and data mart transformations (adjust the connection and execute SQL at the final stage).
