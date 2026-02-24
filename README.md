# 🏨 Hotel-Analytic-Dashboard--Snowflake-Tableau
Data pipeline using Snowflake (Bronze/Silver/Gold Layer)  with Snowsight and Tableau for the Data visualization

## 📌 Project Summary
This project is a data engineering and business intelligence study that transforms raw hotel booking data into actionable insights. The data was cleaned and transformed on **Snowflake** using the **Medallion Architecture (Bronze, Silver, Gold)** layers and visualized into an interactive dashboard using **Snow Sight** &&  **Power BI**.

## 📊 Project Visuals (Dashboard)
The final dashboard prepared in Snowflake ,Snowsight and Tableau analyzes revenue, occupancy rates, and booking trends for decision makers.

<img width="744" height="432" alt="image" src="https://github.com/user-attachments/assets/47e6c48e-599e-44a2-94e5-9297a4e5af01" />



### 🔗 Live Dashboard

You can view the interactive Tableau dashboard here:

👉 **[View Hotel Analytics Dashboard](https://public.tableau.com/app/profile/henry.tirla/viz/HotelBooking_17719416527260/HotelAnalyticsDashboard)**



---

## 🛠 Tech Stack
* **Data Warehouse:** Snowflake
* **ETL & Data Modeling:** SQL (DDL, DML, Data Quality Checks)
* **Visualization (BI):** Tableaux, Snowflake Snowsight
* **Data Architecture:** Medallion Architecture (Bronze -> Silver -> Gold)

---

## 🏗 Data Pipeline & Architecture

The data pipeline consists of the following layers:

### 1. Bronze Layer (Raw Data)
* Raw data in CSV format was ingested into Snowflake using the `COPY INTO` command.
* All columns were stored as `STRING` to prevent data loss during ingestion.

### 2. Silver Layer (Cleaned & Transformed Data)
* **Data Quality Checks:** Invalid emails, negative amounts, and inconsistent dates (Check-out < Check-in) were filtered out.
* **Data Type Conversions:** Data types were corrected using functions like `TRY_TO_DATE` and `TRY_TO_NUMBER`.
* **Standardization:** Names were standardized using `INITCAP` and emails using `LOWER` functions.

### 3. Gold Layer (Business Ready Data)
* Business-specific tables (Data Marts) were created for reporting needs.
* `GOLD_AGG_DAILY_BOOKING`: Cumulative daily data for time series analysis.
* `GOLD_AGG_HOTEL_CITY_SALES`: City-based performance analysis.

---

## 📈 Snowsight and Tableau
The following KPIs and analyses were created using data fetched from Snowflake:
* **Key KPIs:** Total Revenue, Total Bookings, Average Booking Amount.
* **Time Analysis:** Revenue tracking on a Year/Quarter/Month basis using drill-down features.
* **Category Analysis:** Distributions based on room types and booking statuses (Cancelled/Confirmed).

---
