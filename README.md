# End-to-End Retail Data Engineering & Analytics Pipeline

[![Python]()]()
[![SQL Server]()]()
[![Pandas]()]()
[![Kaggle API]()

## 📖 Project Overview
This project establishes a comprehensive **ELT (Extract, Load, Transform)** pipeline that automates the transition of raw retail transactional data into actionable business intelligence. It covers everything from API-based ingestion to advanced analytical reporting using SQL.



---

## 🎯 Business Problem Statement
In modern retail, data is often siloed or "dirty" (missing values, inconsistent naming, improper types). This project solves these challenges by:
1.  **Automating Data Retrieval**: Moving away from manual CSV downloads to API-driven extraction.
2.  **Data Quality Assurance**: Cleansing and normalizing raw data to ensure accurate financial reporting.
3.  **Insight Generation**: Answering critical business questions regarding Year-over-Year (YoY) growth and regional performance.

---

## 🏗️ Technical Workflow

### Phase 1: Data Ingestion & Engineering (Python)
* **Automated Extraction**: Integrated **Kaggle API** to pull real-time retail datasets.
* **Advanced Cleaning**: 
    * Standardized column naming conventions (Snake Case).
    * Handled null values and "Unknown" entries.
    * Created derived metrics: `Discount`, `Sale Price`, and `Total Profit`.
    * Cast `Order Date` into optimized `datetime` objects for time-series analysis.
* **Database Ingestion**: Utilized `SQLAlchemy` to load the processed dataset into **Microsoft SQL Server**, ensuring schema optimization by adjusting `NVARCHAR` lengths.

### Phase 2: Analytical SQL (T-SQL)
* Implemented **CTEs** (Common Table Expressions) for query modularity.
* Leveraged **Window Functions** (`ROW_NUMBER`) for regional ranking.
* Applied **Aggregate Logic** to compare Month-over-Month (MoM) sales performance.

---

## 📂 Repository Structure
| File | Description |
| :--- | :--- |
| `data_pipeline.ipynb` | Jupyter Notebook containing Python ETL logic. |
| `sql_code.sql` | T-SQL script containing the 5 major business insights. |
| `requirements.txt` | List of Python dependencies. |

---

## 📊 Business Insights Derived
The analysis phase answers the following high-value questions:
1.  **Top Revenue Drivers**: Identification of the top 10 products by total revenue.
2.  **Regional Leadership**: Top 5 best-selling products in each geographical region.
3.  **Growth Metrics**: Comparison of 2022 vs. 2023 sales performance by month.
4.  **Category Trends**: Identifying the peak sales month for each product category (Furniture, Office Supplies, Technology).
5.  **Profitability Analysis**: Sub-categories with the highest percentage growth in profit (2023 vs. 2022).

---
