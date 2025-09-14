````markdown
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

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/nyc-taxi-etl.git
   cd nyc-taxi-etl
````

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the ETL pipeline**

   ```bash
   jupyter notebook notebooks/ETL_pipeline.ipynb
   ```

---

## 🌐 Cloud Storage

The processed dataset is uploaded to AWS S3:

```
s3://etl-demo-mani/processed/yellow_tripdata_clean.csv
```

---

## 📌 Key Learnings

* Designed and executed a complete ETL workflow (Extract → Transform → Load).
* Integrated **AWS S3** with Python (boto3) for cloud-based storage.
* Demonstrated how **SQL indexing** can drastically improve query performance.
* Built the pipeline to be **Postgres-ready**, making it scalable for production systems.

---

## 📜 License

This project is open-source and available under the MIT License.
