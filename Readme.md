# 🚕 Uber Taxi Trip Data Analysis using Python (EDA Project)

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on an **Uber Data Analytics** containing **10,000 trip records**.

The goal of this project is to analyze taxi ride data using **Python**, **Pandas**, **Matplotlib**, and **Seaborn** in order to:

- understand trip patterns
- clean and validate raw data
- create useful derived features
- visualize trends and distributions
- identify outliers
- explore fare, duration, and distance relationships
- generate business insights from trip-level taxi data

> **Note:** This project focuses only on **data analysis (EDA)** and does **not include machine learning model creation, training, or testing**.

---

# 🧰 Tools & Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

# 📂 Dataset Information

The dataset contains taxi trip-level information with the following columns:

- `VendorID`
- `tpep_pickup_datetime`
- `tpep_dropoff_datetime`
- `passenger_count`
- `trip_distance`
- `pickup_longitude`
- `pickup_latitude`
- `RatecodeID`
- `store_and_fwd_flag`
- `dropoff_longitude`
- `dropoff_latitude`
- `payment_type`
- `fare_amount`
- `extra`
- `mta_tax`
- `tip_amount`
- `tolls_amount`
- `improvement_surcharge`
- `total_amount`

### Sample Dataset Size

- **Total Records:** ~10,000 rows
- **Format:** CSV

---

# 🎯 Project Objectives

This project was built to practice and demonstrate:

- Loading and inspecting CSV data using Pandas
- Cleaning real-world transportation data
- Working with datetime columns
- Creating new features such as trip duration
- Performing univariate and bivariate analysis
- Detecting outliers in numeric columns
- Understanding taxi demand patterns by hour and weekday
- Exploring payment and tipping behavior
- Visualizing pickup and dropoff coordinate patterns
- Generating portfolio-ready EDA insights

---

# 🏗️ Project Workflow

The notebook follows a structured EDA workflow:

1. **Import Libraries**
2. **Load Dataset**
3. **Inspect Dataset Structure**
4. **Check Missing Values**
5. **Convert Date Columns**
6. **Create New Features**
7. **Clean Invalid Records**
8. **Univariate Analysis**
9. **Outlier Detection**
10. **Time-Based Analysis**
11. **Payment Type Analysis**
12. **Vendor Analysis**
13. **Geospatial Basic Analysis**
14. **Correlation Analysis**
15. **Relationship Analysis**
16. **Summary Insights**
17. **Export Cleaned Dataset**

---

# 🧹 Data Cleaning Performed

The following cleaning steps were applied:

- Converted pickup and dropoff timestamps to **datetime**
- Created **trip duration in minutes**
- Removed rows with:
  - zero or negative trip duration
  - zero or negative trip distance
  - negative fare amount
  - negative total amount

A cleaned version of the dataset was stored separately for downstream analysis.

---

# ⚙️ Feature Engineering

The following new columns were created:

- **`trip_duration_minutes`**  
  Difference between pickup and dropoff timestamps

- **`pickup_hour`**  
  Extracted hour from pickup timestamp

- **`pickup_day`**  
  Day of the month from pickup timestamp

- **`pickup_weekday`**  
  Day name (Monday, Tuesday, etc.)

- **`pickup_month`**  
  Month extracted from pickup timestamp

- **`fare_per_mile`**  
  Fare amount divided by trip distance

- **`total_per_mile`**  
  Total amount divided by trip distance

---

# 📊 Analysis Performed

## 1. Univariate Analysis

Analyzed distributions of:

- Passenger count
- Trip distance
- Fare amount
- Total amount
- Trip duration

### Visualizations Used:

- Count plots
- Histograms
- KDE plots

---

## 2. Outlier Detection

Checked outliers in:

- Trip distance
- Fare amount
- Trip duration

### Visualizations Used:

- Boxplots

---

## 3. Time-Based Analysis

Analyzed taxi demand and fare behavior by:

- Pickup hour
- Weekday

### Visualizations Used:

- Line plots
- Count plots

---

## 4. Payment Analysis

Explored:

- Payment type distribution
- Average tip amount by payment type

### Payment Type Mapping Used:

- `1 = Credit card`
- `2 = Cash`
- `3 = No charge`
- `4 = Dispute`
- `5 = Unknown`
- `6 = Voided trip`

---

## 5. Vendor Analysis

Compared:

- Number of trips by vendor
- Average total amount by vendor

---

## 6. Geospatial Basic Analysis

Visualized:

- Pickup coordinates
- Dropoff coordinates

### Visualizations Used:

- Scatter plots (sampled for performance)

---

## 7. Relationship Analysis

Explored relationships between:

- Trip distance vs fare amount
- Trip distance vs total amount
- Trip duration vs total amount

### Visualizations Used:

- Scatter plots
- Correlation heatmap

---

# 📈 Key Insights / Report Summary

Below are the main findings from the analysis:

## 🚕 Trip Behavior

- Most taxi trips appear to be **short to medium-distance rides**, which is expected in dense urban transportation.
- Trip duration is concentrated around shorter rides, indicating typical city travel patterns.

## 💵 Fare & Revenue Patterns

- **Fare amount** generally increases as **trip distance increases**.
- **Total amount** also rises with **trip duration**, though not always linearly.
- Longer trips tend to contribute more revenue but may also include tolls and extra charges.

## 👥 Passenger Patterns

- Most rides are likely dominated by **single passengers or small groups**, which is common in taxi usage.

## ⏰ Demand by Time

- Taxi demand varies by **hour of the day**, helping identify possible peak travel times.
- Weekday trends can help reveal operational demand patterns.

## 💳 Payment & Tips

- Payment method distribution shows how customers prefer to pay.
- Tip behavior differs across payment types, especially between **credit card** and **cash**.

## 🏢 Vendor Comparison

- Vendor-level trip counts and average total amount may reveal operational differences between service providers.

## 📍 Location Patterns

- Pickup and dropoff scatter plots help identify common geographic concentration zones.

## 📦 Outliers

- Real-world transportation datasets naturally contain outliers in:
  - trip distance
  - fare amount
  - trip duration

These outliers may represent:

- airport rides
- toll-heavy rides
- traffic delays
- premium/long-distance trips

---

# 📌 Business Value of This Analysis

This project demonstrates how EDA can support:

- **Fare trend understanding**
- **Taxi demand pattern analysis**
- **Driver operation insights**
- **Revenue behavior analysis**
- **Payment and tipping behavior analysis**
- **Data cleaning before predictive modeling**
- **Preparation for future machine learning tasks**

---

# 💼 Resume / Portfolio Description

You can use this project in your resume as:

**Uber Data Analysis using Python**

- Performed **Exploratory Data Analysis (EDA)** on **10,000 NYC taxi trip records** using **Python, Pandas, Matplotlib, and Seaborn**.
- Applied **data cleaning, datetime conversion, feature engineering, outlier analysis, time-based trend analysis, payment insights, vendor comparison, geospatial scatter analysis, and correlation analysis**.
- Built a **portfolio-ready Jupyter Notebook project** to understand taxi fare behavior, trip duration patterns, and demand trends.
