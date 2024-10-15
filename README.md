# Wedge Transaction Data Project

This project involves processing and summarizing transaction data from the Wedge cooperative. The tasks include uploading data to Google BigQuery, generating a sample of owner transactions, and creating summary tables in an SQLite database.

## Tasks

1. **Task 1: Upload Data to Google BigQuery**  
   Upload all Wedge transaction records to Google BigQuery and handle data types and null values.

2. **Task 2: Generate a Sample of Owners**  
   Extract a sample of owner transactions (excluding non-owners) and save it to a local file.

3. **Task 3: Build Summary Tables**  
   Create summary tables for sales trends and store them in an SQLite database.

## How to Run

1. Ensure you have Python installed with required libraries.
2. Connect to your Google BigQuery instance.
3. Run the Python scripts for each task.

## Files

- **task1_bigquery_upload.py**: Handles uploading transaction records to Google BigQuery.
- **task2_sample_owners.py**: Generates a sample of owner transactions.
- **task3_summary_tables.py**: Creates summary tables and stores them in SQLite.
