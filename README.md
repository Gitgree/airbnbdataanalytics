Project Components
1. mock_data_in_cosmosdb.py

This Python script generates mock Airbnb customer and booking data and inserts it into Azure Cosmos DB.
It serves as the data ingestion layer, simulating a real-world source system.

Key Features:

Generates realistic sample data using Python libraries.

Inserts data into Azure Cosmos DB containers.

Supports data partitioning for scalability.

Demonstrates schema design for customer_dim and bookings_fact.

2. synapse_table_creation.sql

This SQL script is executed in Azure Synapse Analytics to create the data warehouse schema and perform aggregations.

Includes:

Schema creation: airbnb

Dimensional tables:

customer_dim — customer-related information

bookings_fact — booking transactions

Aggregated table:

BookingCustomerAggregation — total bookings and amount per country

Stored Procedure:

BookingAggregation — truncates and refreshes aggregation results

⚙️ Workflow

Data Generation: Run the Python script to populate mock data in Cosmos DB.

Data Movement: Data from Cosmos DB can be ingested into Synapse using Azure Data Factory or Synapse Pipelines.

Data Modeling: Execute the SQL script in Synapse to create and aggregate data.

Analytics: Query aggregated data for insights such as total bookings and revenue by country.

🧠 Learning Objectives

Understand data modeling in Synapse (star schema design).

Learn how to ingest and analyze data from Cosmos DB.

Practice ETL/ELT pipeline design with Azure components.

Automate data refresh using stored procedures.

🗂️ Folder Structure
├── mock_data_in_cosmosdb.py       # Python script for generating and inserting mock data
├── synapse_table_creation.sql     # SQL script for Synapse schema and procedures
├── README.md                      # Project documentation

🚀 Future Enhancements

Automate Cosmos DB → Synapse ingestion using Azure Data Factory.

Add visualization layer using Power BI.

Incorporate real-time updates with Event Hubs or Stream Analytics.

🧑‍💻 Author

Uddipan Goswami
Cloud Engineer | Data Enthusiast | Azure & Python Developer
