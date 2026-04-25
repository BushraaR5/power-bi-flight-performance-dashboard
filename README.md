# power-bi-flight-performance-dashboard
End-to-end Power BI dashboard analyzing flights, airline and airport performance. Covers delay patterns, cancellations, on-time performance (OTP), and operational drivers using a structured data model and DAX.

# ✈️ Flight Performance Dashboard (Power BI)

## 🚀 Dashboard Preview

<img width="1372" height="742" alt="image" src="https://github.com/user-attachments/assets/00bf293a-afad-4ecb-829b-5bc35bf5d510" />

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

<img width="337" height="495" alt="image" src="https://github.com/user-attachments/assets/3b2862ae-c10e-4277-9ec3-e487899cab26" />



- Total flights, OTP %, delay rate, cancellations
- Monthly performance trends
- Delay and cancellation drivers

👉 Key insight:

- **Late Aircraft delays dominate (~40%)**, indicating cascading operational impact
- **Weather is the primary cause for cancellations (>50%)**

---

### 🔹 2. Delay Analysis

<img width="470" height="487" alt="image" src="https://github.com/user-attachments/assets/145348c7-001f-47e0-9827-1cf3bf782315" />


- Delay trends by cause (Air System, Airline, Late Aircraft)
- Departure vs arrival delay comparison
- Time-of-day heatmap

👉 Key insight:

- **Delays peak in early morning (1–3 AM)** → spillover from previous schedules

---

### 🔹 3. Airline Analysis

<img width="611" height="506" alt="image" src="https://github.com/user-attachments/assets/4af0e888-7f2f-47ae-a46f-bf19db40c756" />


- Airline performance vs OTP and fleet size
- Delay distribution by airline
- Best/worst performing airlines

👉 Key insight:

- Larger airlines show **higher late aircraft dependency**, while smaller airlines have more balanced delay causes

---

### 🔹 4. Airport Analysis

<img width="506" height="482" alt="image" src="https://github.com/user-attachments/assets/561ad8cf-7165-445a-aa4b-ca2e19079a44" />


- Airport efficiency vs traffic volume
- Delay drivers per airport
- Best and worst performing airports

👉 Key insight:

- High-traffic airports show **greater delay variability**, indicating scalability challenges

---

### 🔹 5. Flight-Level Explorer

<img width="1341" height="507" alt="image" src="https://github.com/user-attachments/assets/31c613c4-645b-476d-912f-32fd67b517c3" />


- Detailed flight records
- Drill-down capability
- Dynamic filtering

👉 Enables granular investigation of delays at individual flight level

---

## 🧭 How to Use the Dashboard

This dashboard is designed to be interactive and user-friendly, enabling both high-level insights and detailed drill-down analysis.

### 🔹 Navigation

* Click the **airplane icon (top-left)** on any page to return to the **Overview page**
* Use the **Back button (top-left)** to return to the previous page after drill-through

### 🔹 Filters & Reset

* Use slicers to filter by airline, airport, date, or time
* Click the **filter icon (top-right)** to **reset all filters** on the current page

### 🔹 Interactive Visuals

* Charts are fully interactive — selecting any element filters the entire page
* In the **Airline Summary**, use the **Delay / Cancellation buttons** to toggle between views

### 🔹 Drill-Through Functionality

* Drill down from summary visuals into the **Flight-Level Explorer**
* The selected filters are dynamically displayed in the page heading
* By default (no filters), the explorer highlights **Late Aircraft delays**

### 🔹 Exploration Tip

* Start from the **Overview page**, then progressively drill into specific airlines, airports, or delay types for deeper insights

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
  <p align="center">
  <img width="177" height="117" alt="image" src="https://github.com/user-attachments/assets/4f86d8f6-8eb3-48fa-9af9-fc3e4136bdd2" />
  </p>
      
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

## ⚙️ Compatibility Notes

* Developed using **Power BI Desktop (Version: 2.153.910.0, 64-bit – April 2026)**
* Opening this file in older versions of Power BI may result in missing features or rendering differences
* It is recommended to use the latest version of Power BI Desktop for full functionality

---

## 📁 Project Structure

- `.pbix` file (Power BI dashboard)
- Data model with fact & dimension tables
- Measures organized in a dedicated DAX table

---

## 📦 Dataset Note

* Due to file size limitations, a **sample dataset** is included in this repository
* The sample data used in this project preserves the structure and logic of the original model
* The full dataset file can be accessed via the link
  🔗 **Download Full Dataset**: [Click here](https://drive.google.com/file/d/1ci4W0pp_bsCgT1ZcDggqb-KrQ1JGxEhx/view?usp=sharing)

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
