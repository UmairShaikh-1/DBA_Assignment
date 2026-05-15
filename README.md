# Databases and Analytics Assignment
This repository contains the analytical work for the NorthStar Urban Mobility and Logistics case study. It includes all code, cleaned datasets and JSON documents required to analyse operational performance, identify inefficiencies, and design a new data architecture.

The project integrates SQL, R, Python, and MongoDB for processing and manipulating data.

# Project Overview
NorthStar is experiencing rising delays, inconsistent performance across hubs, and fragmented data systems.

This project rebuilds the organisation’s data system:
* Integrating nine operational datasets
* Cleaning and standardising inconsistent fields
* Detecting missing links and contradictions
* Analytical performance metrics (delays, speeds, failure flags)
* Analysing delays, failures, and cost inefficiencies
* Preparing nested JSON documents for MongoDB
* Demonstrating CRUD operations and query optimisation
* Providing insights and recommendations for operational improvement

# Technologies Used
* R (sqldf, dplyr, ggplot2)
* Python (pandas, seaborn, matplotlib, json)
* MongoDB (PyMongo, NoSQL document modelling)
* Google Colab for execution
* GitHub for version control and documentation

# R: SQL Queries & Analytics
The R scripts demonstrate:
* SQL queries executed inside R using sqldf
* Filtering, joining, grouping, and aggregating operational data
* Visualisations including:
    * Delays over time
    * Complaints by hub
    * Route distance distributions
    * Delivery distance histograms

These analyses reveal delay factors, hub‑level inefficiencies, and route‑specific performance issues.

# Python: Data Processing & Integration
The Python notebook performs:
* Full dataset loading and inspection
* Standardisation of zones, timestamps, and categorical fields
* Detection of missing links (orders without deliveries, incidents without valid delivery IDs)
* Engineering of new metrics:
    * delay_minutes
    * avg_speed_kmph
    * failure_flag
    * has_complaint_history
* Integration of drivers, vehicles, and hubs into a unified master dataset
* Performance, delay, failure, and cost analysis
* Visual analytics (top delayed routes, failure rates, delay trends, cost vs delay)

This forms the analytical backbone of the project.

# MongoDB: NoSQL Modelling & CRUD Operations
MongoDB is used to store nested operational histories that relational databases cannot represent efficiently.

The repository includes:
* Nested JSON documents for orders, deliveries, and complaints
* Python scripts for:
    * Uploading documents into MongoDB
    * Running CRUD operations
    * Updating complaint statuses
    * Retrieving delayed orders and high‑severity complaints

This demonstrates how MongoDB supports real‑time operational workflows.

# Query Optimisation
The query_optimization.py script shows how indexing improves MongoDB performance.

Key results:
* Querying delayed orders dropped from scanning 1250 documents to 202
* Querying by order_id switched from COLLSCAN to IXSCAN
* Execution plans verified using explain()
* This proves the importance of indexing for scalability and responsiveness.

# Key Insights
Across all tools, the analysis revealed:
* Widespread delays (average 572 minutes)
* High failure rates on specific hubs and routes
* Cost inefficiencies on long routes
* Fragmented systems causing missing links and inconsistent records
* Need for hybrid relational + NoSQL architecture

These insights directly informed the recommendations in the final report.

# How to Use This Repository
1. Clone the repository
2. Open the R scripts for SQL and visual analytics
3. Run the Python notebooks in Google Colab
4. Upload JSON files to MongoDB using the provided scripts
5. Explore CRUD operations and query optimisation examples

# Author
Mohammad Umair  

Module: Databases and Analytics
