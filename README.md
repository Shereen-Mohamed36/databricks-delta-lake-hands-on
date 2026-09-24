#  Delta Lake Hands-on Operations with Databricks

## Overview
A hands-on implementation exploring core **Delta Lake** features and table management operations using **PySpark** on **Databricks**. This task demonstrates practical data engineering concepts such as ACID compliance, schema governance, historical auditing, and time travel.

---

## Tech Stack
* **Platform:** Databricks (PySpark, Delta Lake APIs)
* **Core Concepts Applied:** ACID Transactions, Upserts (`MERGE`), Schema Enforcement, Schema Evolution, Transaction Logging, and Time Travel.

---

## Implemented Tasks & Steps
1. **Table Initialization:** Created the initial `orders` Delta table and ingested base transactional data.
2. **Incremental Append:** Ingested new daily order batches and verified row counts.
3. **Data Modification:** Performed conditional updates and deletions on active and cancelled orders.
4. **Upserts (`MERGE`):** Implemented idempotent batch updates and inserts to handle concurrent modifications without duplicates.
5. **Schema Governance:** 
   * Tested **Schema Enforcement** to block invalid data types and prevent data corruption.
   * Applied **Schema Evolution** (`mergeSchema`) to safely integrate new columns (`discount`) into the existing table structure.
6. **Auditing & Time Travel:** 
   * Inspected transaction history via `DESCRIBE HISTORY` to review atomic operations.
   * Leveraged **Time Travel** (`versionAsOf`) to query older table snapshots and recover historical states.

---

## 📁 Repository Structure
```text
databricks-deltalake-handson/
│
├── notebooks/
│   └── delta_lake_orders_pipeline.ipynb   # PySpark Databricks Notebook
│
├── documentation/
│   └── databricks_Task.pdf         # Detailed step-by-step report with execution screenshots
│
└── README.md
