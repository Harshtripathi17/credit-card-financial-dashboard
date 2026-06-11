<!-- @format -->

# 💳 Credit Card Financial Performance Dashboard

## Project Overview

This project delivers a comprehensive, interactive **Credit Card Financial Performance Dashboard** developed in **Power BI**. It provides real-time, actionable insights into key financial metrics, customer demographics, and transactional behaviors.

To showcase a robust, enterprise-level data pipeline, the dataset was ingested, structured, and queried within a **MySQL Relational Database**, and subsequently integrated into Power BI via an **ODBC Connection Layer**.

---

## Tech Stack & Architecture

- **Data Source:** Raw CSV files (Transaction & Customer Profile Data).
- **Database Management:** MySQL Server (Data Storage, Schema Creation, and Custom SQL Scripting).
- **Connectivity Interface:** Open Database Connectivity (ODBC) Driver.
- **BI & Data Visualization:** Power BI Desktop (DAX, Data Modeling, and UX/UI Design).

---

## Data Pipeline & Technical Implementation

### 1. Database Ingestion & SQL Querying

Instead of loading flat files directly into Power BI, raw CSV files were imported into a **MySQL instance** to simulate a real-world production environment and practice direct relational querying.

Two main tables were engineered:

- `credit_card_detail`: Tracking transactional attributes (Revenue, Interest, Swipe Fees, Utilization Rate).
- `customer_detail`: Storing customer profile metrics (Age, Income, Education, Job, Dependent Count).

Custom optimized SQL queries were written to preprocess, filter, and structure the data streams before loading them into the BI reporting environment.

### 2. Overcoming Connectivity Challenges: The ODBC Solution

> **Technical Problem-Solving Encountered:** > When directly connecting Power BI to the MySQL instance, native connector compatibility or driver mismatches can frequently interrupt data streams.
>
> **The Solution:** To establish a bulletproof, stable pipeline, I manually configured an **ODBC (Open Database Connectivity) Data Source Name (DSN) link**. By using the MySQL ODBC Unicode Driver, I bypassed native connector bottlenecks, successfully establishing a stable, authenticated handshake between Power BI and the MySQL relational engine.

---

## Key Business Insights & Analytical Findings

### Financial Overview (YTD)

- **Total Revenue:** $55 Million
- **Total Interest Earned:** $7.8 Million

### Crucial Discoveries & Demographics

- **Top Card Tier:** The **Blue Card** is the primary driver of corporate profitability, accounting for **$46 Million** of total revenue.
- **Core Customer Segment:** High-value customers aged **40–50 years old** represent the highest revenue-generating bracket, contributing nearly **$25 Million**.
- **Gender Dynamics:** Male cardholders led overall transaction metrics, contributing **$31 Million** to revenue, compared to **$26 Million** from Female cardholders.
- **Top Geographic Drivers:** **Texas (TX), New York (NY), and California (CA)** represent the top three states, combining for roughly **70%** of the entire active portfolio performance.
- **Channel Acquisition:** **Delinquency / Churn risk / Defaulters** remains low, while overall transaction swipes showed a steady **2.8% WoW (Week-over-Week) growth** matrix.

---
