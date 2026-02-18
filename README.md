# Lab 1: Explore Azure SQL Database

DP-900T00-A Introduction to Microsoft Azure Data [Cloud Slice Provided], Learning Path 02 (CSS)

# 📌 Project Overview

In this lab, I provisioned and explored Azure SQL Database. I created a new SQL server, deployed a sample AdventureWorks database, configured firewall rules, and connected using both the Query Editor in the Azure portal and SQL Server Management Studio (SSMS). I executed SQL queries to explore tables, retrieve data, and understand relationships between entities.

By completing this lab, I gained hands-on experience in provisioning, querying, and managing cloud relational databases.

# 🎯 Business Objectives

Provision a relational database in Azure for development and learning.

Explore sample datasets to understand schema, relationships, and SQL querying.

Learn best practices for database configuration, networking, and security.

# 📊 Analytical Approach
# 1️⃣ Provision Azure SQL Database

Created a SQL server with SQL authentication.

Configured public endpoint access and added client IP to firewall rules.

Deployed the AdventureWorks sample database for immediate exploration.

# 2️⃣ Explore and Query Data

Examined tables and relationships in the database.

Ran queries to inspect and aggregate data:

SELECT * FROM SalesLT.Product;
SELECT ProductID, Name, ListPrice, ProductCategoryID FROM SalesLT.Product;


Performed JOIN operations to combine data across tables:

SELECT 
    p.ProductID, 
    p.Name AS ProductName,
    c.Name AS Category, 
    p.ListPrice
FROM SalesLT.Product AS p
INNER JOIN SalesLT.ProductCategory AS c 
    ON p.ProductCategoryID = c.ProductCategoryID;

# 3️⃣ Resource Management & Cleanup

Deleted the resource group containing the SQL server and database.

Reinforced best practices for cost management and secure resource lifecycle.

# 💡 Insights Gained

Azure SQL Database simplifies provisioning and administration of relational databases.

Sample databases accelerate learning and support hands-on SQL practice.

Proper firewall and network configuration is essential for secure access.

# 🛠 Skills Demonstrated

Provisioning Azure SQL Database.

Executing SQL queries and joins.

Exploring database schema and relationships.

Managing cloud resources efficiently.

# 🔮 Recommendations / Next Steps

Practice complex queries, aggregations, and stored procedures.

Connect SQL Database to Power BI for reporting and visualization.

Explore performance tuning and indexing strategies.

# 🚀 Why This Project Matters

This lab provided practical exposure to cloud-based relational database management, foundational SQL querying, and real-world dataset exploration—core skills for analytics and database administration.


# Lab 2: Explore Azure Storage for Non-Relational Data

DP-900T00-A Introduction to Microsoft Azure Data [Cloud Slice Provided], Learning Path 03 (CSS)

# 📌 Project Overview

In this lab, I provisioned an Azure Storage Account and explored non-relational data options, including Blob Storage, Table Storage, and Queue Storage. I uploaded files, created tables for structured data, and sent messages to queues to understand asynchronous communication patterns.

By completing this lab, I learned how to store, manage, and interact with unstructured and semi-structured data in Azure.

# 🎯 Business Objectives

Explore differences between relational and non-relational storage.

Store, retrieve, and query data using Azure Storage services.

Understand cloud storage security and access management.

# 📊 Analytical Approach
# 1️⃣ Provision Azure Storage Account

Created a standard general-purpose v2 storage account.

Enabled Blob, Table, and Queue storage services.

Generated access keys to securely connect client applications.

# 2️⃣ Explore Blob Storage

Created containers for CSV and JSON datasets.

Uploaded sample files and inspected them in Azure portal and Storage Explorer.

Practiced downloading, uploading, and viewing data programmatically.

# 3️⃣ Explore Table Storage

Created a table for structured key-value data.

Inserted sample entities and queried rows based on partition and row keys.

Learned that Table Storage supports lightweight queries without relational joins.

# 4️⃣ Explore Queue Storage

Created a queue for messaging scenarios.

Sent messages into the queue and retrieved them to observe the enqueue/dequeue lifecycle.

# 5️⃣ Resource Management & Cleanup

Deleted storage account to avoid ongoing costs.

Reinforced secure access, key management, and resource lifecycle best practices.

# 💡 Insights Gained

Azure Storage offers flexible solutions for unstructured, semi-structured, and messaging data.

Blobs store files, Tables support key-value storage, and Queues enable asynchronous message handling.

Secure access management and proper container organization are essential for production scenarios.

# 🛠 Skills Demonstrated

Provisioning Azure Storage accounts and services.

Uploading and managing data in Blob, Table, and Queue storage.

Performing key-value queries and handling message queues.

Managing access keys and performing cleanup efficiently.

# 🔮 Recommendations / Next Steps

Explore Azure Data Lake Storage Gen2 for hierarchical data and analytics workloads.

Integrate storage data with Synapse or Power BI for analysis.

Implement automated pipelines using Azure Functions and queues.

# 🚀 Why This Project Matters

This lab provided hands-on experience with cloud-native non-relational storage, a core skill for IoT, big data, and modern analytics applications.


# Lab 3: Explore Fundamentals of Large-Scale Data Analytics

DP-900T00-A Introduction to Microsoft Azure Data [Cloud Slice Provided], Learning Path 04 (CSS)

# 📌 Project Overview

In this lab, I provisioned an Azure Synapse Analytics workspace and a Spark pool, ingested sample datasets, and explored batch and streaming analytics. I used Kusto Query Language (KQL) to query tables in Data Explorer pools, summarized and filtered data, and practiced working with real-time and historical datasets.

By completing this lab, I gained hands-on experience with large-scale data processing in the cloud.

# 🎯 Business Objectives

Understand Azure Synapse Analytics and Spark pools for big data processing.

Explore batch and streaming data pipelines.

Query large datasets and analyze time-series data using KQL.

# 📊 Analytical Approach
# 1️⃣ Provision Azure Synapse Workspace

Created workspace with associated Data Lake Storage Gen2.

Opened Synapse Studio to manage development, compute, and data ingestion.

# 2️⃣ Create Spark Pool

Created an Apache Spark pool named sparkpool.

Configured memory-optimized nodes and enabled autoscaling.

Attached notebooks to Spark pool for executing structured streaming jobs.

# 3️⃣ Ingest and Explore Data

Uploaded sample CSV files for IoT device readings.

Ingested batch datasets and enabled stream ingestion in Data Explorer pools.

Queried tables to verify and inspect imported data.

# 4️⃣ Query and Analyze Data

Used KQL to filter, summarize, and aggregate time-series data:

devices
| summarize AvgVal = avg(Value) by Device
| sort by Device asc


Practiced filtering by device and time windows to analyze trends.

# 5️⃣ Resource Management & Cleanup

Deleted Synapse workspace, Spark pool, and Data Explorer pools.

Reinforced cost control and resource lifecycle management best practices.

# 💡 Insights Gained

Synapse Analytics allows scalable processing of large datasets with both batch and streaming methods.

Spark Structured Streaming and Delta tables enable real-time analytics.

KQL provides fast and powerful querying for time-series and IoT data.

Cloud big data processing workflows differ significantly from local analytics, emphasizing scalability.

# 🛠 Skills Demonstrated

Provisioning and configuring Synapse Analytics and Spark pools.

Ingesting and exploring batch and streaming datasets.

Querying data with KQL and analyzing time-series datasets.

Managing cloud resources efficiently.

# 🔮 Recommendations / Next Steps

Explore integration with Power BI for visualization of large datasets.

Experiment with more complex streaming scenarios and Delta Lake features.

Build hybrid analytics pipelines combining batch and streaming data.

# 🚀 Why This Project Matters

This lab provided practical experience in large-scale cloud analytics, developing skills in data ingestion, processing, and analysis at enterprise scale—a foundational capability for cloud-based data engineering and analytics careers.
