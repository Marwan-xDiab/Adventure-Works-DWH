# Building Sales Data Mart
 

## General Info
<B>Incremental load </B> , only the data that has changed since the last extraction is loaded into the DWH. Data that has already been loaded and has not changed is not extracted and does not need to be deleted before a new load.

<B>Full load </B>, entire data dump that takes place the first time a data source is loaded into the warehouse

<B>Slowly Changing Dimension (SCD) </B> is a dimension that stores and manages both current and historical data over time in a data warehouse. It is considered and implemented as one of the most critical ETL tasks in tracking the history of dimension records.

## Introduction
About Project Info
After extracting new and updated data from the AdventureWorks2019 (OLTP data) database, create a star schema and load data to dimensions and fact tables after transforming the data, and finally apply full, incremental, and slow-changing dimension (SCD) loading. 

## Data Sources
- ### AdventureWorks2014 (OLTP) from Microsoft https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms
  - Customer
  - Product
  - SalesTerritory
  - SalesOrderHeader  
  - SalesOrderDetail
  - PersonPhone
  - BusinessEntityAddress
  - Person
  - ProductModel
  - ProductModelProductDescriptionCulture
  - ProductDescription
  - Production
  - ProductSubcategory
  - ProductCategory

- ### EO_AdventureWorksDW2014 (DWH) 
  - dim_customer
  - dim_date  
  - dim_territory
  - dim_product 
  - lookup_country
  - meta_control_table
  - fact_sales  

## Using ETL Tools
- SSIS SQL Server Integration Services
- SQL Server 
- C# Language 
- Data Modeling (SQL)


## Steps 
1- <B>Data Modeling (Star Schema)</B>

![Capture](https://user-images.githubusercontent.com/90741989/205361677-9809f5c6-23e8-4505-a043-ed3e0c220d97.PNG)

2- <B>Slowly Changing Dimension (SCD) </B>

![Capture](https://user-images.githubusercontent.com/90741989/205362208-ce6b2782-4aab-4a8c-966a-5b7c6befd7fe.PNG)

3- <B>Full load </B>

![1](https://user-images.githubusercontent.com/90741989/205362695-e8d88307-2483-45c6-8735-d1cf5915ea5f.PNG)

4- <B>Incremental load</B>

![2](https://user-images.githubusercontent.com/90741989/205362700-b9e8b019-bd54-48f2-a9e0-3ec4101fd160.PNG)



