# power-bi-flight-performance-dashboard
Power BI dashboard analyzing flight operations across airlines, airports, and routes. Covers delay patterns, cancellations, on-time performance (OTP), and operational drivers using a structured data model and DAX.

## 📊 Live Insights from Flight Operations Data

This Power BI dashboard analyzes airline performance, delay patterns, and airport efficiency using a structured data model and advanced analytics.

# ✈️ Flight Performance Dashboard (Power BI)

## 📌 Project Overview

This project analyzes **flight performance, delays, and cancellations** using a structured data model built in Power BI.

The dataset includes **flight-level records**, along with **airline and airport data**, enabling a multi-dimensional analysis of operational efficiency across the aviation network.

The goal is to:

- Identify key drivers of delays and cancellations
- Compare airline and airport performance
- Understand temporal patterns in flight operations
- Build a scalable and optimized data model

---

## 🧠 Business Problem

Airlines and airports operate in a highly complex environment where delays and cancellations impact:

- Customer experience
- Operational efficiency
- Cost management

This dashboard answers key questions:

- What are the **primary causes of delays**?
- Which airlines and airports perform best/worst?
- How do delays vary **over time and across locations**?
- Are delays driven by **operations or external factors (e.g., weather)**?

---

## 🏗️ Data Model (Star Schema)

A structured data model was built using multiple related tables:

### 🔹 Fact Table

- `Flights` → flight-level data (delays, status, timestamps)

### 🔹 Dimension Tables

- `Airlines` → airline details
- `Airports` → airport metadata
- `Date Table` → time intelligence
- `Time Table` → hourly analysis

👉 Relationships were designed to enable efficient filtering and scalable analysis.

---

## ⚙️ Data Preparation (Power Query)

Data was cleaned and transformed using Power Query:

- Removed unused columns to optimize model size
- Created calculated columns (e.g., delay flags, time buckets)
- Standardized formats (date/time transformations)
- Built reusable transformation steps (ETL pipeline)

---

## 📊 Dashboard Pages & Features

### 🔹 1. Overview

- Total flights, OTP %, delay rate, cancellations
- Monthly performance trends
- Delay and cancellation drivers

👉 Key insight:

- **Late Aircraft delays dominate (~40%)**, indicating cascading operational impact

---

### 🔹 2. Delay Analysis

- Delay trends by cause (Air System, Airline, Late Aircraft)
- Departure vs arrival delay comparison
- Time-of-day heatmap

👉 Key insight:

- **Delays peak in early morning (1–3 AM)** → spillover from previous schedules

---

### 🔹 3. Airline Analysis

- Airline performance vs OTP and fleet size
- Delay distribution by airline
- Best/worst performing airlines

👉 Key insight:

- Larger airlines show **higher late aircraft dependency**, while smaller airlines have more balanced delay causes

---

### 🔹 4. Airport Analysis

- Airport efficiency vs traffic volume
- Delay drivers per airport
- Best and worst performing airports

👉 Key insight:

- High-traffic airports show **greater delay variability**, indicating scalability challenges

---

### 🔹 5. Flight-Level Explorer

- Detailed flight records
- Drill-down capability
- Dynamic filtering

👉 Enables granular investigation of delays at individual flight level

---

## 🧮 Key Metrics (DAX)

Custom measures were created for:

- On-Time Performance (OTP)
- Delay Rate %
- Cancellation %
- Top Delay Reason
- Target vs Actual comparisons

👉 Advanced DAX concepts used:

- Context transition
- Dynamic ranking (TOPN)
- Conditional calculations

---

## 🎨 Dashboard Design

- Dark theme for better readability
- Consistent color coding:
    - 🟢 Good
    - 🟡 Average
    - 🔴 Bad
    - 🔵 Delay causes
- KPI cards for quick insights
- Interactive slicers for exploration

---

## ⚡ Performance Optimization

- Removed unused columns in Power Query
- Organized measures into a dedicated table
- Optimized relationships and model size

---

## 📈 Key Insights

- Late Aircraft is the **primary delay driver (~40%)**
- Delays are largely **operational**, while cancellations are **weather-driven**
- Early morning delays indicate **schedule spillover effects**
- Larger airlines face **turnaround dependency issues**
- High-volume airports show **scalability constraints**

---

## 🛠️ Tools Used

- Power BI
- Power Query (ETL)
- DAX (Data Analysis Expressions)

---

## 📁 Project Structure

- `.pbix` file (Power BI dashboard)
- Data model with fact & dimension tables
- Measures organized in a dedicated DAX table

---

## 🚀 What This Project Demonstrates

- End-to-end dashboard development
- Data modeling (star schema)
- Advanced DAX calculations
- Data storytelling & business insights
- Performance optimization

---

## 📬 Use Case

This dashboard can be used by:

- Airline operations teams
- Airport management
- Data analysts exploring operational efficiency

---

## 🔗 Future Improvements

- Real-time data integration
- Predictive delay modeling
- Drill-through analysis for root cause investigation

---

## 👤 Author

Bushraa Rahim
