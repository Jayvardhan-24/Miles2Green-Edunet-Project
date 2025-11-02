# 🌱 Miles2Green: Smart Insights for Sustainable Mobility

## 📘 Project Overview
**Miles2Green** is an initiative aimed at promoting *eco-friendly driving habits and energy-efficient vehicle usage* through data-driven insights. The project leverages electric vehicle (EV) trip data to analyze patterns in energy consumption, driving behavior, and trip characteristics — ultimately helping to build smarter and greener transportation systems.

The project aligns with green skills development by combining **data analytics** and **machine learning** to understand how factors such as trip distance, time of day, and driving patterns influence energy efficiency.

---

## 🗓️ Week 1: Data Collection and Preprocessing

### 🔹 Objective
The focus for **Week 1** was to collect, understand, and prepare datasets for analysis. This stage ensures data quality and consistency before any modeling or visualization tasks.

### 🔹 Steps Performed
1. **Data Collection:**
   - Two datasets were gathered:
     - **Electric Vehicle Trip Energy Consumption Data**
     - **EV Specifications Data**
   - Both datasets were integrated for exploratory analysis and feature correlation.

2. **Data Preprocessing:**
   - Removed missing or duplicate records.  
   - Standardized column names for consistency.  
   - Converted data types (e.g., `Trip Distance` to numeric, `Time of Day` to categorical).  
   - Detected and treated outliers in `Trip Energy Consumption`.  
   - Scaled numerical features for uniformity in future modeling.  
   - Encoded categorical variables such as `Day of the Week`.

This preprocessing pipeline prepared the dataset for efficient visualization and modeling in subsequent weeks.

---

## 📊 Dataset Description

### 1. **Electric Vehicle Trip Energy Consumption Data**
Contains trip-level details that describe how energy is consumed under different conditions:
| Feature | Description |
|----------|--------------|
| **Trip Energy Consumption (kWh)** | The energy consumed for each trip. |
| **Vehicle ID** | Unique identifier for each vehicle. |
| **Trip Distance (km)** | Distance covered during the trip. |
| **Time of Day** | Departure hour of the trip. |
| **Day of the Week** | Day when the trip occurred. |
| **Longitude** | Average longitude representing trip location. |

### 2. **EV Specifications Data**
Provides technical details about various electric vehicles:
| Feature | Description |
|----------|--------------|
| **Vehicle ID** | Unique vehicle identifier (matches the Trip Data). |
| **Battery Capacity (kWh)** | Total battery capacity of the EV. |
| **Vehicle Model** | Name/model of the EV. |
| **Manufacturer** | Brand producing the EV. |
| **Range (km)** | Maximum distance achievable per charge. |

Together, these datasets provide both **operational** (trip-based) and **technical** (vehicle-based) perspectives necessary for analyzing green driving performance.

---

## ⚙️ Next Steps
- Perform **exploratory data analysis (EDA)** to identify trends and patterns.
- Develop **predictive models** to estimate energy efficiency and environmental impact.
