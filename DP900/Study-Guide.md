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
• Describe common formats for data files
• Describe types of databases

### Describe common data workloads
• Describe features of transactional workloads
• Describe features of analytical workloads

### Identify roles and responsibilities for data workloads
1. Describe responsibilities for database administrators
    - manage databases, assign permissions to users, store backup copies of data and restore data in the event of a failure  
2. Describe responsibilities for data engineers
    - manage infrastructure and process for data integration across the organization, applying data cleaning routines, identifying governance rules, and implementing pipelines to transfer and transform data between systems.  
3. Describe responsibilities for data analysts
    - explore and analyze data to create visualizations and charts that enable organizations to make informed decisions 

## Identify considerations for relational data on Azure (20—25%)
### Describe relational concepts
• Identify features of relational data
• Describe normalization and why it is used
• Identify common structured query language (SQL) statements
• Identify common database objects

### Describe relational Azure data services
• Describe the Azure SQL family of products including Azure SQL Database, Azure SQL
• Managed Instance, and SQL Server on Azure Virtual Machines
• Identify Azure database services for open-source database systems

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
• Identify use cases for Azure Cosmos DB
• Describe Azure Cosmos DB APIs

## Describe an analytics workload on Azure (25—30%)
### Describe common elements of a modern data warehouse
• Describe considerations for data ingestion and processing
• Describe options for analytical data stores
• Describe Azure services for data warehousing, including Azure Synapse Analytics, Azure
Databricks, Azure HDInsight, and Azure Data Factory
### Describe consideration for real-time data analytics
• Describe the difference between batch and streaming data
• Describe technologies for real-time analytics including Azure Stream Analytics, Azure Synapse
Data Explorer, and Spark structured streaming
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


