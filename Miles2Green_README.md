# 🌱 Miles2Green: Smart Insights for Sustainable Mobility

## 📘 Project Overview
**Miles2Green** is an AI-driven system designed to promote sustainable electric vehicle (EV) driving.
It analyzes driving patterns to provide personalized eco-driving insights and converts the driver’s journey data into an AI-generated sustainability story, visualizing how much carbon emission was saved compared to traditional fuel vehicles.

This project integrates machine learning for driving analytics and generative AI for storytelling, motivating users to drive efficiently and contribute to a greener environment.
---
## ⚙️ Working & Functionalities
1. Eco-Driving Analyzer:
Collects or simulates driving data (speed, distance, acceleration, braking frequency, energy use, etc.). Processes data to calculate an Eco-Score based on efficiency metrics. Identifies driving behavior (smooth, aggressive, idle-heavy).
Generates personalized feedback such as:
“Reducing harsh braking by 10% could extend your range by 15 km.”

2. Carbon Footprint Story Generator:
Calculates total CO₂ saved by comparing EV usage to an equivalent petrol/diesel vehicle. Converts raw statistics into a narrative summary using a generative AI model (e.g., GPT-based): “This week, your green driving prevented 8 kg of CO₂ emissions — enough to power a home fan for 30 hours!”

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

# Week 2 - Machine Learning Model Development

This week focused on building a predictive machine learning model for the Miles2Green project. The goal was to develop a simple yet effective model capable of predicting electric vehicle (EV) trip energy consumption. This prediction will support personalized eco-driving insights and sustainability storytelling.

## Objectives Completed

* Understand the structure and purpose of both datasets
* Perform essential preprocessing and data cleaning
* Visualize key patterns to validate data quality
* Build and evaluate baseline predictive ML models
* Generate insights to validate model performance

---

## Datasets Used

* **EV_Energy_Consumption_Dataset.csv** – Time-series EV telemetry data
* **Electric Vehicle Trip Energy Consumption Data.csv** – Trip-level summary data

The predictive model was built primarily using the trip-level dataset.

---

## Preprocessing & Data Cleaning

The following steps were performed to clean and prepare the data:

### Basic Cleaning

* Removed duplicate rows
* Handled missing values:

  * Numeric values → filled with median
  * Categorical values → filled with mode
* Corrected data types (e.g., converting timestamps)

### Outlier Removal

* Removed extreme outliers using Interquartile Range (IQR) method for:

  * Trip Distance
  * Trip Energy Consumption
  * Trip Time Length

### Encoding & Scaling

* Applied Label Encoding for categorical columns (e.g., Day of Week)
* Scaled numerical features using StandardScaler

---

## Visualization & Data Understanding

To extract insights and validate the data, the following visualizations were generated:

* **Histogram** of the target variable (Trip Energy Consumption)
* **Correlation heatmap** for feature relationships
* **Scatter plot** of Trip Distance vs Energy Consumption
* **Boxplot** of Trip Distance to confirm outlier removal

These plots helped confirm data consistency and identify meaningful feature relationships.

---

## Model Development

Two regression models were built and compared:

### 1. Linear Regression

* Served as a baseline model
* Provided quick interpretability

### 2. Random Forest Regressor

* Captured nonlinear relationships
* Typically more robust

Both models were trained on an 80/20 train-test split.

---

## 📈 Model Evaluation

Evaluation metrics used:

* **MAE (Mean Absolute Error)**
* **MSE (Mean Squared Error)**
* **R² Score**

### Final Results

**Linear Regression:**

* MAE: 0.2862
* MSE: 0.1595
* R² Score: 0.8434

**Random Forest Regressor:**

* MAE: 0.2439
* MSE: 0.1189
* R² Score: 0.8832

➡️ Random Forest demonstrated the best performance and was selected as the final model.

---

## Insights

* Strong relationship observed between **Trip Distance** and **Energy Consumption**
* Model successfully captures patterns and trends in the dataset
* R² score above 0.88 indicates high reliability for prediction

---

## Week 2 Summary

This week successfully completed all essential steps for building the predictive ML model:

* Cleaned and prepared the dataset
* Performed exploratory data analysis
* Built baseline and advanced regression models
* Evaluated model performance with industry-standard metrics
* Selected the best-performing model (Random Forest)

This lays the foundation for Week 3, where insights and model predictions will be used to generate AI-driven sustainability stories.

---

Next Step: **Story generation & integrating predictions into Miles2Green narrative engine.**
