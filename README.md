# 🚀 Airbnb Market Intelligence & Revenue Optimization Dashboard

🔗 **Interactive Dashboard:** [View Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiOGI1NGViNTMtZWY3NS00YzE1LTk3ZGEtNDM5YmI1NmRmM2E2IiwidCI6IjZiNGQwNDQ4LTc5MGMtNGQ5MS1iZjY3LTg5ZDk1NmJlNDEwYSJ9) (View In Landscape Mode On Phone)

---

## 📌 Problem Statement

This dashboard provides a comprehensive analysis of Airbnb listings across NYC neighbourhoods to uncover **market demand, pricing behavior, host concentration, and listing performance trends**.

By evaluating listing availability, reviews, room types, pricing, and host activity, it enables stakeholders to:

- Understand **which neighbourhoods drive the highest demand**
- Identify **top-performing and underperforming listings**
- Monitor **pricing behavior across room types and locations**
- Analyze **host concentration and listing ownership patterns**
- Support **revenue optimization and occupancy decisions**

---

## 📊 Key Metrics (KPIs)

The dashboard tracks key indicators such as:

- **Total Listings**: Total number of Airbnb properties
- **Total Hosts**: Unique hosts in the marketplace
- **Average Price**: Average listing price across NYC
- **Total Reviews**: Total customer engagement volume
- **Demand Indicator**: Review-based demand classification
- **Performance Category**: High, Low, No Activity, Average

---

## 🎯 Business Requirements

- Neighbourhood-wise **listing and host concentration**
- **Room type pricing analysis**
- Demand segmentation using **reviews and availability**
- Identification of **top hosts by reviews and listings**
- Visual comparison of **price vs customer engagement**
- Highlighting **top & bottom performing listings**
- Interactive filtering with **slicers**

---

## 🔧 Workflow & Technical Steps

### 1️⃣ Data Acquisition & Cloud Storage

- Imported raw Airbnb NYC dataset (CSV)
- Uploaded dataset into **AWS S3 bucket**
- Used S3 as **landing zone / data lake layer**

---

### 2️⃣ AWS IAM & Snowflake Integration

![S3 Bucket - ](https://github.com/ShouryaSrivastav/Airbnb-Project/blob/65b0ca97f266b3a30f90e89348fb9b81df42cb0a/First%20Page%20Airbnb%20Project.png)
![IAM Role - ](https://github.com/ShouryaSrivastav/Airbnb-Project/blob/65b0ca97f266b3a30f90e89348fb9b81df42cb0a/First%20Page%20Airbnb%20Project.png)
![Integration - ](https://github.com/ShouryaSrivastav/Airbnb-Project/blob/c7226f0d8304e4bbf61a37c4d1bf0caeb30761fc/Integration.png)
![Loading Data - ](https://github.com/ShouryaSrivastav/Airbnb-Project/blob/c7226f0d8304e4bbf61a37c4d1bf0caeb30761fc/Loading%20Data.png)

- Created **IAM role and trust policy**
- Configured **S3 read permissions**
- Built **Snowflake storage integration**
- Created **external stage**
- Loaded data using **COPY INTO command**

---

### 3️⃣ Data Cleaning & Transformation (Snowflake SQL)

![Data Cleaning 1 - ](https://github.com/ShouryaSrivastav/Airbnb-Project/blob/c7226f0d8304e4bbf61a37c4d1bf0caeb30761fc/Data%20Cleaning.png)
![Data Cleaning 2 - ](https://github.com/ShouryaSrivastav/Airbnb-Project/blob/c7226f0d8304e4bbf61a37c4d1bf0caeb30761fc/Data%20CLeaning%202.png)

Performed scalable cleaning inside Snowflake:

- Removed invalid or zero prices
- Standardized host names
- Trimmed listing names
- Validated listing IDs
- Checked null neighbourhood values
- Created **Demand Category**
- Created support fields for performance logic

---

### 4️⃣ Power BI + Power Query Setup

- Connected cleaned Snowflake table to **Power BI Desktop**
- Performed **light semantic cleanup in Power Query**
- Fixed data types and display formatting
- Built user-friendly slicer columns
- Applied a **premium dark UI theme**
- Designed **2 interactive pages**

---

### 5️⃣ Advanced DAX Measures

Created advanced business measures:

- Total Listings
- Total Hosts
- Average Price
- Total Reviews
- Performance Category
- Top Performer Flag
- Rank High / Rank Low
- Demand Indicator
- Top & Bottom Listing Logic

---

## 📊 Dashboard Preview & Insights

### 📄 Page 1 — Airbnb Market Overview

**Visuals:** KPI cards, neighbourhood listing distribution, pricing trends, room type comparison

**Key Insights:**  
Provides a high-level view of market concentration, room type demand, and pricing trends.

![Page 1 — Overview](https://github.com/ShouryaSrivastav/Airbnb-Project/blob/65b0ca97f266b3a30f90e89348fb9b81df42cb0a/First%20Page%20Airbnb%20Project.png)

---

### 📄 Page 2 — Market Insights & Performance

**Visuals:**  
- Demand indicator  
- Price vs reviews scatter plot  
- Top hosts by reviews  
- Top hosts by listings  
- Listing performance segmentation  
- Top & bottom performers  

**Key Insights:**  
Highlights demand behavior, pricing effectiveness, host concentration, and listing optimization opportunities.

![Page 2 — Performance](https://github.com/ShouryaSrivastav/Airbnb-Project/blob/65b0ca97f266b3a30f90e89348fb9b81df42cb0a/Second%20Page%20Airbnb%20Project.png)

---

## 🛠️ Tools & Technologies

- **AWS S3**
- **AWS IAM**
- **Snowflake SQL**
- **Power Query Editor**
- **Power BI Desktop**
- **DAX**
- **Data Modeling**
- **Dashboard Storytelling**

---

## ✅ Conclusion

The **Airbnb Market Intelligence & Revenue Optimization Dashboard** demonstrates a complete **cloud analytics + BI workflow**:

1. Raw CSV → AWS S3
2. Secure Snowflake integration via IAM
3. SQL cleaning & feature engineering
4. Power BI semantic modeling
5. Interactive dashboard storytelling

It transforms listing-level data into actionable market intelligence, enabling **pricing optimization, host analysis, occupancy tracking, and revenue-focused decision-making**.

---
