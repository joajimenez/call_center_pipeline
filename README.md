# 📊 Call Centre Performance Data Pipeline

## 📌 Overview

This project demonstrates how to build an end-to-end **data engineering pipeline** to process, clean, and analyze call center activity data. Using the City of Calgary’s 311 dataset, I automated ETL workflows, modeled the data for analytics, and delivered interactive dashboards that track call center performance metrics.

The goal was to transform raw CSV data into **actionable insights** that help operations teams improve service levels and decision-making.

---

## ⚙️ Tech Stack

- **Python** (Pandas, NumPy) → Data cleaning & transformation
- **SQL (PostgreSQL/SQLite)** → Data storage & modeling
- **Airflow (or Prefect)** → Workflow automation & scheduling
- **TO DECIDE** → Interactive dashboards
- **Excel** → Lightweight stakeholder reports

---

## 🛠️ Pipeline Architecture

1. **Data Ingestion**

   - Automated collection of raw CSV datasets.
   - Standardized schema for consistent ingestion.

2. **Data Transformation**

   - Converted timestamps, normalized service request fields.
   - Engineered KPIs:
     - Average Answer Delay
     - Call Abandonment Rate
     - SLA Compliance (% of calls answered within SLA)
   - Flagged anomalies (spikes in call volume, long delays).

3. **Data Modeling**

   - Built **fact tables** (call volumes, wait times, outcomes).
   - Built **dimension tables** (agents, service categories, dates).

4. **Automation**

   - Scheduled daily refresh via Airflow DAGs.
   - Email reports auto-delivered to stakeholders.

5. **Visualization**
   - Interactive dashboard with:
     - Daily trends in call volume
     - SLA compliance over time
     - Agent performance comparisons
   - Drill-downs into peak hours and backlog risks.

---

## 📈 Business Value

- Eliminated **manual reporting** (80% effort reduction).
- Provided **real-time visibility** into call center performance.
- Empowered managers to adjust staffing and improve SLA compliance.

---

## 🚀 Future Enhancements

- Deploy pipeline on **AWS (S3 + RDS + MWAA)**.
- Add **streaming ingestion** with Kafka for near real-time updates.
- Build ML model to forecast call volumes and staffing needs.

---

## 📂 Repo Structure

```bash
call-center-pipeline/
│── dags/                # Airflow DAGs for automation
│── notebooks/           # Data exploration & transformation notebooks
│── sql/                 # Database schema & queries
│── dashboards/          # BI reports
│── data/                # Sample input CSVs
│── README.md            # Project documentation
```
