# 🚖 NYC Taxi ETL Pipeline — Python + SQL + AWS S3

## 📌 Overview
This project demonstrates an **end-to-end ETL pipeline** for large-scale data processing, optimization, and cloud storage integration.

- **Extract**: Pulled **1.5M+ NYC Yellow Taxi records (Jan 2024)** from Parquet format.
- **Transform**: Cleaned invalid trips, standardized datetimes, and engineered new features (trip duration).
- **Load**: Stored processed data into **SQLite** (schema compatible with Postgres for production use).
- **Cloud Integration**: Uploaded the cleaned dataset to **AWS S3** for scalable storage and sharing.
- **Optimization**: Applied SQL indexing, reducing query execution time by **94%**.

---

## ⚙️ Tech Stack
- **Languages**: Python, SQL  
- **Libraries**: Pandas, SQLAlchemy, Boto3  
- **Database**: SQLite (Postgres-ready)  
- **Cloud**: AWS S3  
- **Environment**: Jupyter Notebook  

---

## 📊 Results
| Step        | Median Time (s) | Mean Time (s) |
|-------------|-----------------|---------------|
| Baseline    | ~0.95           | ~0.93         |
| Indexed     | ~0.06           | ~0.05         |

✅ Achieved a **94% reduction** in query execution time after indexing the `pickup_datetime` column.

---

