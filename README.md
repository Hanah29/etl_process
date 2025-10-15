
#  ETL Data Pipeline using Python, Pandas, and PostgreSQL

This project implements a **data pipeline (ETL process)** that extracts a large dataset from a CSV file, transforms and cleans the data using **Pandas**, and efficiently loads it into a **PostgreSQL** database.

---

##  Overview

The goal of this assignment is to design and implement an ETL (Extract, Transform, Load) process capable of handling **large-scale datasets** (2+ million records).  
The pipeline is modular, memory-efficient, and built to run safely and repeatedly without duplicating data.

### Key Features
-  **Chunked data extraction** — handles large files without exhausting memory.  
-  **Data transformation** — renames columns, fixes date formats, fills missing values.  
-  **Bulk loading** — inserts data efficiently into PostgreSQL using `execute_values()`.  
-  **Error handling** — automatic rollback on insert errors.  
-  **Environment configuration** — secure credentials via `.env` file.

---

##  Architecture


CSV File  →  Pandas (Extract & Transform)  →  PostgreSQL (Load)


| ETL Step | Description | Implementation |
|-----------|--------------|----------------|
| **Extract** | Read CSV file in chunks | `pandas.read_csv(chunksize=...)` |
| **Transform** | Clean, rename, and format data | `transform_chunk()` |
| **Load** | Bulk insert into PostgreSQL | `psycopg2.extras.execute_values()` |

---

##  Setup Instructions

### 1️ Clone the Repository
```bash
git clone https://github.com/yourusername/etl-pipeline.git
cd etl-pipeline

### 2️ Install Dependencies

Use a virtual environment or install directly:

pip install pandas psycopg2-binary python-dotenv

### 3️ Configure Environment Variables

Create a .env file in the project root:

DB_NAME=your_database
DB_USER=your_username
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
TABLE_NAME=your_table_name
CSV_PATH=/path/to/your/large_dataset.csv
CHUNK_SIZE=10000



---

##  Technologies Used

* Python 3.10+
* Pandas
* Psycopg2
* PostgreSQL
* python-dotenv





## Team Members

| Name                | ID       |
|---------------------|----------|
| Hermela Gashaw      | 1401389  |
| Hana Ayalew         | 1401373  |
| Etsub Zewdu         | 1401215  |
| Kidistemariam Getinet | 1401544 |
| Eyerusalem Chernet  | 1401229  |
csv file download link-https://www.datablist.com/learn/csv/download-sample-csv-files#people-dataset 
