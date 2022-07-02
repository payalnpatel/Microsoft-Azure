# DP-900 Study Guide
Study Guide / Notes created using: https://docs.microsoft.com/en-us/users/23110622/collections/0kjyh8rn5x76j6

## Describe core data concepts (25—30%)
### Describe ways to represent data
1. Describe features of structured data: 
    - adheres to a fixed schema, so all the data has the same fields/properties 
    - commonly in tabular structure - data represented in one or more tables that consists of rows to represent an instance of a data entity, and columns to represent attributes of the entity. 
    - often stored ina database / relational model 
2. Describe features of semi-structured
    - information that has some structure, but allows for some variation between entity instances 
    - i.e. JSON (JavaScript Object Notation) 
3. Describe features of unstructured data
    - i.e. documents, images, audio and video data, and binary files that may not have a specific structure 

### Identify options for data storage
1. Describe common formats for data files
    - CSV - fields seperated by commas and rows terminated by a new line
    - JSON - each attribute might be an object or collection of objects
    - XML (extensible markup language) - uses tags enclosed in angle brackets to define elements and attributes
    - Binary Large Object (BLOB) - files stored as binary data (1s and 0s) - images, video, audio, and app-specific docs
    - optimized file formats - enable compression, indexing, and efficient storage and processing 
        - Avro - row-based format created by Apache. each record contains a header that describe the structure of the data in the record.  header is stored as JSON.  data is stored as binary information. app uses info in the header to parse the binary data and extract the fields it contains. good format for compressing data and minimizing storage and network bandwidth requirements
        - ORC (optimized row columnar format) - organizes data into columns rather than rows - developed by HortonWorks for optimizing read and write operations in Apache Hive. ORC file contains stripes of data. each stripe holds the data for a column or set of columns. a stripe contains an index into the rows in the stripe, the data for each row, and a footer that holds statistical info for each column
        - Parquet - another columnar data format. created by Cloudera and Twitter. contains row groups.  data for each column is stored together in the same rwo group. each row group contains one or more chunks of data. includes metadata that describes the set of rows found in each chunk. specializes in storing and processing nested data types efficiently.  supports very efficient compression and encoding schemas.  
2. Describe types of databases
    - a database is used to define a central system in which data can be stored and queried 
    - relational database - commonly used to store and query structured data. data stored in tables represent entities. each instance of an entity is assigned a primary key (PK) that uniquely identifies it, and these keys are used to reference the entity instance in other tables. tables are managed and queried using SQL 
    - non-relational database - data management system that does not apply a relational schema to the data. often referred to as NoSQL database, even though some support a variant of the sql lanugage. 
        - key-value databases - each record consists of a unique key and an associated value, which can be any format
        - document database - specific form of key-value database in which the value is a JSON document (or other document)
        - column family database - stores tabular data comprising rows and columns but you can divide the columns into groups known as column families. each column family can hold a set of columns that are logically related together. 
        - graph database - stores entities as nodes with links to define relationships between them 

### Describe common data workloads
1. Describe features of transactional workloads
    - a transactional system records transactions that encapsulate specific events the organization wants to track (think of a transaction as a small, discrete, unit of work) 
    - transactional systems are often high-volume, sometimes handling millions of transactions per day. 
    - the work performed by transactional systems is often referred to as Online Transactional Processing (OLTP) 
    - OLTP solutions rely on a database system in which data storage is optimized for both read and write operations in order to support transactional workloads in which data are received through CRUD operations (create, retrieve, update, delete) 
    - OLTP systems enforce transactions that support so called ACID semantics 
        - Atomicity - each transaction is treated as a single unit, which succeeds completely or fails completely 
        - Consistency - transactions can only take the data in the database from one valid state to another
        - Isolation - concurrent transactions cannot interfere with one another, and must result in a consistent database state
        - Durability - when a transaction has been committed, it will remain committed. 
    - OLTP systems are typically used to support live apps that process business data (LOB apps) 
2. Describe features of analytical workloads
    - typically uses read-only (or read-mostly) systems that store vast volumes of historical data or business metrics. analytics can be based on a snapshot of data at any given point in time, or a series of snapshots 
    - an OLAP model is an aggregated type of data storage that is optimized for analytical workloads. 
  
### Identify roles and responsibilities for data workloads
1. Describe responsibilities for database administrators
    - manage databases, assign permissions to users, store backup copies of data and restore data in the event of a failure  
2. Describe responsibilities for data engineers
    - manage infrastructure and process for data integration across the organization, applying data cleaning routines, identifying governance rules, and implementing pipelines to transfer and transform data between systems.  
3. Describe responsibilities for data analysts
    - explore and analyze data to create visualizations and charts that enable organizations to make informed decisions 

## Identify considerations for relational data on Azure (20—25%)
### Describe relational concepts
1. Identify features of relational data
    - Relational tables are a format for structured data, each row in a table has the same columns.  each column stores data of a specific data type. 
    - in a relational database, you model collections of entities from the real world as tables. an entity can be anything for which you want to record information.  A table contains rows, and each row represents a single instance of an entity. 
2. Describe normalization and why it is used
    - A term used by database professionals for a schema design process that minimizes data duplication and enforces data integrity. 
    - Normalization involves:
        - separate each entity into its own table
        - separate each discrete attribute into its own column
        - uniquely identify each entity instance (row) using a PK 
        - use FK columns to link related entities 
3. Identify common structured query language (SQL) statements - ddl, dml etc 
    - SQL - Structured Query Language - used to communicate with a relational database, the standard language for relational database management systems. 
    - standardized by ANSI in 1986 and ISO in 1987. 
    - variety of dialects of SQL due to proprietary extensions created by different vendors. popular dialects of SQL include:
        - transact-SQL (T-SQL) - used by Microsoft SQL Server and Azure SQL Services
        - pgSQL - PostgreSQL
        - PL/SQL - used by Oracle. PL/SQL stands for Procedural Language/SQL 
    - SQL Statements are grouped into 3 main logical groups:
        - Data Definition Language (DDL) - used to create, modify, and remove tables and other objects in a database (table, stored procedures, views, etc.) 
            - CREATE
            - ALTER
            - DROP
            - RENAME 
        - Data Control Language (DCL) - used to manage access to objects in a database by granting, denying, or revoking permissions to specific users or groups.
            - GRANT
            - DENY
            - REVOKE
        - Data Manipulation Language (DML) - used to manipulate rows in tables. enable you to query, insert new rows, or modify existing rows.  can also delete rows if you don't need them. 
            - SELECT
            - INSERT
            - UPDATE
            - DELETE
4. Identify common database objects
    - View - a view is a virtual table based on the results of a SELECT query. can think of a view as a window on specified rows in one or more underlying tables.
    - Stored Procedure - a stored procedure defines SQL statements that can be run on command. stored procedures are used to encapsulate programmatic logic in a database for actions that applications need to perform when working with data. 
    - Index - an index helps you search for data in a table. think of an index over a table like an index at the back of a book. an index consumes storage space, and each time you insert, update, or delete data in a table, the indexes for the table must be maintained. 

### Describe relational Azure data services
1. Describe the Azure SQL family of products including Azure SQL Database, Azure SQL Managed Instance, and SQL Server on Azure Virtual Machines
    - Azure SQL Database - a fully managed, highly scalable PaaS database service. Azure SQL database is available as a Single Database or an Elastic Pool. 
    - Azure SQL Managed Instance - a PaaS option that provides near 100% compatibility with on-prem SQL server instances while abstracting the underlying hardware and OS.
    - SQL Server on Azure Virtual Machines - a virtual machine running in Azure with an installation of SQL server.  the use of a VM makes this an IaaS solution that virtualizes hardware infrastructure for compute, storage, and networking in Azure. Great option for lift and shift migration of existing on-prem SQL server installations. 
    - Azure SQL Edge - SQL engine that is optimized for IoT scenarios that need to work with streaming time-series data 
2. Identify Azure database services for open-source database systems
    - MySQL 
    - MariaDB - built-in support for temporal data. a table can hold several versions of data, enabling an app to query the data as it appeared at some point in the past
    - PostgreSQL - allows you to store custom data types, with their own non-relational properties.  store and manipulate geometric data, such as lines, circles and polygons. pgsql 
    
## Describe considerations for working with non-relational data on Azure (15—20%)
### Describe capabilities of Azure storage
1. Describe Azure Blob storage
    - scalable, cost-effective storage for binary files 
    - a service that enables you to store massive amounts of unstructured data as binary large objects, or blobs, in the cloud.  blobs are an efficient way to store data files in a format that is optimized for cloud-based storage, and apps can read and write them by using the Azure blob storage API. 
    - can store blobs in containers in an Azure storage account. a container provides a way of grouping related blobs together. can control who can read/write blobs inside a container at the container level. 
    - within a container you can organize blobs in a hierarchy of virtual folders
    - 3 different types of blob
      1. block blobs - a block blob is handled as a set of blocks. best used to store discrete, large, binary objects that change infrequently. 
      2. page blobs - a page blob is organized as a collection of fixed size 512-byte pages.  optimized to support random read write operations. use to implement virtual disk storage for VMs 
      3. append blobs - a block blob that is optimized ti support append operations 
    - 3 access tiers for blob storage (to help balance access latency and storage cost)
      1. hot tier (default) - blobs that are accessed frequently
      2. cool tier - lower performance and incurs reduced storage charges; for data that is accessed infrequently
      3. archive tier - provides the lowest storage cost, but with increased latency.  intended for historical data that must not be lost. 
2. Describe Azure File storage
    - network file shares such as you would typically find in corporate networks 
    - a file share enables you to store a file on one computer and grant access to that file to users and applications running on other computers 
    - Azure Files is a way to create cloud-based network shares. can create Azure file storage in a storage account
    - Azure File Storage has 2 performance tiers
      1. Standard tier - uses hard disk-based hardwdare in a datacenter
      2. Premium tier - uses solid-state disks - greater throughput but at a higher rate 
    - Azure File supports 2 common network file sharing protocols 
      1. Server Message Block (SMB) - file sharing is commonly used across multiple OS (Windows, Linux, macOS) 
      2. Network File System (NFS) shares are used by some Linux & macOS versions.  To create an NFS share, you must use a premium tier storage account and create and configure a virtual network through which access to the share can be controlled. 
3. Describe Azure Table storage
    - key-value storage for applications that need to read and write data values quickly 
    - a NoSQL storage solution that makes use of tables containing key/value data items.  each item is represented by a row that contains columns for the data fields that needs to be stored
    - enables you to store semi-structured data.
    - no concepts of FKs, relationships, stored procedures, views or other objects you might find in relational db 
    - data is usually denormalized, with each row holding the entire data for a logical entity 
    - splits a table into partitions to enable fast access. 
    - partitioning is a mechanism for grouping related rows, based on a common property or partition key. rows that share the same partition key will be stored together.
    - partitioning helps organize the data, improve scalability and performance in the following ways":
      1. partitions are independent of each other
      2. can search for data using the partition key 
    - key in Azure Table Storage consists of 2 elements: the partition key and a row key 

### Describe capabilities and features of Azure Cosmos DB
1. Identify use cases for Azure Cosmos DB
    - Azure Cosmos DB supports multiple APIs that enable developers to use the programming semantics of many common kinds of data store to work with data in a Cosmos DB Database. 
    - uses indexes and partitioning to provide fast read and write performance and scale to massive volumes of data. 
    - highly scalable database management system 
    - automatically allocates space in a container for your partitions, and each partition can grow up to 10GB in size. 
    - indexes are created and maintained automatically.
    - highly suitable for IoT and Telematics, Retail and marketing, gaming, web and mobile applications 
2. Describe Azure Cosmos DB APIs
    - enable developers to migrate data from commonly used NoSQL stores and apply their existing programming skills
    - Core (SQL) API - native API in Cosmos DB manage data in JSON document format, and despite being a NoSQL data storage solution, uses SQL syntax to work with the data
    - MongoDB API - a popular open source database in which data is stored in binary JSON (BSON) format
    - Table API - used to work with data in key-value tables, similar to Azure Table Storage 
    - Cassandra API - compatabile with Apache Cassandra that uses column-family storage structure 
    - Gremlin API - used with data in a graph structure; in which entities are defined as vertices that form nodes in connected graph. Nodes are connected by edges that represent relationships 

## Describe an analytics workload on Azure (25—30%)
### Describe common elements of a modern data warehouse
1. Describe considerations for data ingestion and processing
    - ETL - Extract, Transform, Load
    - ELT - Extract, Load, Transform 
    - Large-scale data ingestion on Azure is best implemented by creating pipelines that orchestrate ETL processes. you can create and run pipelines using Azure Data Factory, or use the same pipeline engine in Azure Synapse Analytics.
    - pipelines consist of one or more activities that operate on data. an input dataset provides the source data, and activities can be defined as a data flow that incrementally manipulates the data until an output dataset is produced. 
    - pipelines use dlinked services to load and process data - enabling you to use the right technology for each step of the workflow. 
2. Describe options for analytical data stores
    - Data warehouses - a relational database in which the data is stored in a schema that is optimized for data analytics rather than transactional workloads. 
        - fact tables - where numeric values are stored 
        - dimension tables - represent entities by which the data can be aggregated 
        - fact and dimension table schema is called a star schema.
        - star schema - often extended into a snowflake schema by adding additional tables related to the dimension tables to represent dimensional hierarchies 
        - great choice when you have transactional data that can be organized into a structured schema of tables, and you want to use SQL to query them 
    - Data lakes - a file store, usually on a distributed file system for high performance data access. technologies like Spark or Hadoop are often used to process queries on the store files and return data for reporting and analytics. these systems often apply a schema-on-read approach to define tabular schemas on semi-structured data files at the point where the data is read for analysis, without applying constraints when it's stored.  great for supporting a mix of structured, semi-structured, and even unstructured data that you want to analyze without the need for schema enforcement when the data is written to the store. 
    - hybrid approaches - combine features of data lakes and data warehouses in a lake database or data lakehouse. 
        - the raw data is stored as files in a data lake, and a relational storage layer abstracts the underlying files and expose them as tables, which can be queried using SQL. 
        - SQL pools in Azure Synapse Analytics include PolyBase, which enables you to define external tables based on files in a datalake (and other sources) and query them using SQL. 
        - Synapse Analytics also supports a lake database approach in which you can use db templates to define the relational schema of your data warehouse, while storing underyling data in data lake storage - separating the storage and compute for your data warehousing solution 
        - data lakehouses - relatively new approach in Spark-based systems, and are enabled through technologies like Delta Lake; which adds relational storage capabilities to Spark, so you can define tables that enforce schemas and transactional consistency, support batch-loaded and streaming data sources, and provide a SQL API for querying.   
3. Describe Azure services for data warehousing, including Azure Synapse Analytics, Azure
Databricks, Azure HDInsight, and Azure Data Factory
    - Azure Synapse Analytics - includes Apache Spark runtime
    - Azure Databricks - built on Apache Spark, and offers native SQL capabilities as well as workload-optimized Spark clusters for data analytics and data science
    - Azure HDInsight 
    - Azure Data Factory - 
    
### Describe consideration for real-time data analytics
1. Describe the difference between batch and streaming data
    - Data processing is the conversion of raw data to meaningful information through a process - 2 general ways to process data include batch processing and stream processing
    - batch processing - multiple data records are collected and stored before being processed together in a single operation. can process on a scheduled time interval, or it could be triggered when a certain amount of data has arrived or as the result of some event. 
        - suitable for handling large datasets efficiently
        - high latency - typically a few hours (latency is time it takes for data to be received and processed) 
        - for complex analytics 
    - stream processing - a source of data is constantly monitored and processed in real time as new data events occur. each new piece of data is processed when it arrives. 
        - intended for individual records or micro batches of few records 
        - low latency - seconds to milliseconds 
        - used for simple response functions, aggregates, or calculations such as rolling averages 
2. Describe technologies for real-time analytics including Azure Stream Analytics, Azure Synapse
Data Explorer, and Spark structured streaming
    - Azure Stream Analytics - PaaS solution you can use to define streaming jobs that ingest data from a streaming source, apply a perpetual query, and write results to output.
        - service for complex event processing and analysis of streaming data. 
    - Spark Structured Streaming - open-source library that enables you to develop complex streaming solutions on Apache Spark Based services in Azure Synapse Analytics, Azure Databricks, and Azure HDInsight 
    - Azure Data Explorer - high performance database and analytics service that is optimized for ingesting and querying batch or streaming data with a time-series element, and which can be used as a standalone Azure service or as an Azure synapse data explorer runtime in Azure Synapse Analytics Workspace 
        - standalone service for efficiently analyzing data. uses KQL 
       
### Describe data visualization in Microsoft Power BI
1. Identify capabilities of Power BI
    - Power BI is a suite of tools and services that data analysts can use to build interactive data visualizations for business users to consume.  Tools include Power BI Desktop, Power BI Service, Power BI Phone App, web browser. 
2. Describe features of data models in Power BI
    - Analytical Modeling in Power BI - use the Model tab of Power BI Desktop to define analytical model by creating relationships between fact and dimension tables, defining hierarchies, setting data types and display formats in the fields tables, and managing other properties of your data. 
    - star schema - fact table related to one or more dimension tables.  
    - dimension tables represent entities by which you want to aggregate numeric values.  numeric measures that will be aggregated by various dimensions in the model are stored in fact tables. each entity is represented by. a row with a unique key value, and each row in a fact table represents a recorded event that has numeric measures associated with it. 
    - attribute hierarchies - enable you to drill-up or drill-down to find aggregated values at different levels in a hierarchical dimension. 
3. Identify appropriate visualizations for data
    - Tables and text - Tables are useful when numerous related values must be displayed, and individual text values in cards can show figures/metrics
    - Bar and column charts - compare numeric values for discrete categories
    - Line charts - examine trends, often over time
    - Pie charts - compare categorized values as proportions of a total 
    - Scatter plots - compare 2 numeric measures and identify a relationship or correlation b/w them
    - Maps - compare values for different geographic areas or locations


