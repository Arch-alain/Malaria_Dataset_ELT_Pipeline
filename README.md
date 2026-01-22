# 🧩 Data Ingestion Pipeline for ClickHouse

This project aims at achieving two objectives:
1. Monitoring the data collection process to keep track of the progress
2. Create a model training and evaluation pipeline 
---

## 🚀 Overview

The pipeline performs the following tasks:

- **Download** Json file from VisionMd
- **Extract**  image data, annotations, and metadata
- **Push** the extracted data to the clickhouse database
- **Download and Insert** the images and classify them in MINIO according to the parasite species

---

## 🏗️ Project Structure

--

### Environment Variables Setup

Create a `.env` file in the project root (this file should be added to `.gitignore`):

```bash
CLICKHOUSE_USER=""
CLICKHOUSE_PASSWORD=""
CLICKHOUSE_DB=""
CLICKHOUSE_HOST=""
CLICKHOUSE_PORT=""
DATA_DIR=""
MINIO_BUCKET = ""
MINIO_ENDPOINT = ""
MINIO_ACCESS_KEY = ""
MINIO_SECRET_KEY =""
LOGS_DIR=""

```

---

## 🧠 Key Components

### 1. `ELT_Process.ipynb`
Handles:
- Json file download from VisionMd Appsuite (`download_file`)
- Data ingestion in ClickHouse
- Images loading in Respective folders in Minio

### Example dependencies:

```
pandas
numpy
polars
clickhouse-driver
requests
python-dotenv
```

---