# Hotel Booking Demand Analysis and Prediction

## Project Overview

This project is a comprehensive data science workflow that analyzes a dataset of hotel booking records to understand key factors influencing booking cancellations and to build a machine learning model to predict them. The project follows a structured approach, from initial data exploration to feature engineering and model preparation, ensuring the final dataset is clean and ready for predictive modeling.

## Project Phases

### Phase 1: Exploratory Data Analysis (EDA) & Data Quality Report

* **Goal:** Understand the structure, content, and quality of the raw data.
* **Key Activities:**
    * Loading and summarizing the dataset (`.info()`, `.describe()`).
    * Identifying and visualizing missing values.
    * Detecting outliers in key numerical columns (`adr`, `lead_time`).
    * Checking for and counting duplicate records.
* **Outcome:** A detailed report highlighting data quality issues, including missing values in `company` and `agent` columns, extreme outliers in `adr`, and a significant number of duplicate rows.

### Phase 2: Data Cleaning (The Core of the Project)

* **Goal:** Address and resolve the data quality issues identified in Phase 1.
* **Key Activities:**
    * **Handling Missing Values:** A strategic approach to impute or handle missing data in `company`, `agent`, `country`, and `children` columns.
    * **Removing Duplicates:** Dropping all identical rows to ensure each booking record is unique.
    * **Handling Outliers:** Capping extreme values in the `adr` column to prevent them from skewing the data distribution.
* **Outcome:** A cleaned, more reliable dataset free of duplicates and with handled missing and outlier values.

### Phase 3: Feature Engineering & Preprocessing

* **Goal:** Transform the cleaned data into a machine learning-ready format.
* **Key Activities:**
    * **Creating New Features:** Generating new, more informative features like `total_guests`, `total_nights`, and `is_family` from existing columns.
    * **Encoding Categorical Variables:** Using one-hot encoding for low-cardinality features and a custom grouping strategy for high-cardinality features like `country`.
    * **CRITICAL STEP: Removing Data Leakage:** Dropping columns like `reservation_status` and `reservation_status_date`, which contain future information and would make the predictive model useless in a real-world scenario.
* **Outcome:** A final, highly processed DataFrame with all necessary features engineered and encoded, ready for model training.

## How to Run the Notebook

To run this notebook, simply upload `hotel_bookings.csv` and `gtc_ml_project1_hotel_bookings__.ipynb` to Google Colab or your local Jupyter environment. Execute the cells sequentially from top to bottom.
