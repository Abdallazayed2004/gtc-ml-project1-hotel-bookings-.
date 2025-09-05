# 🏨 Hotel Booking Demand Analysis

### **📌 Project Overview**

This repository contains an in-depth analysis of the **Hotel Booking Demand** dataset. The project walks through a comprehensive data science workflow, from initial data cleaning and exploratory data analysis (EDA) to preprocessing techniques. The goal is to deeply understand customer booking behavior, identify key drivers of demand, and prepare the dataset for downstream machine learning modeling
---

### **📂 Dataset**

* **Source:** Hotel Booking Demand (Kaggle)
* **Records:** Approximately 119,000 hotel bookings.
* **Features:** 32 attributes, including reservation details, customer demographics, arrival dates, and outcomes like cancellation status.

---

### **🔑 Key Steps**

#### **Data Cleaning & Preprocessing**
* **Data Import & Inspection:** The initial step involved loading the dataset and performing a preliminary review of its structure, data types, and basic descriptive statistics.
* **Handling Missing Values:** Missing data was systematically addressed. We utilized libraries like `missingno` to visualize the distribution of missing values, which revealed a concentration in features such as `agent` and `company`. These values were then handled appropriately (e.g., imputation or removal) to maintain data integrity.
* **Duplicate and Inconsistency Removal:** We identified and removed duplicate records and corrected inconsistencies within the dataset to ensure a clean and reliable foundation for analysis.

#### **Outlier Analysis**
* **Detection:** The **Interquartile Range (IQR)** method was applied to detect anomalies in key numerical features, including `adr` (Average Daily Rate) and `lead_time`. This step helped in identifying unusually high or low values that could skew analysis.
* **Visualization:** Boxplots were used to visualize the distributions of these features, providing a clear representation of the presence and magnitude of outliers.

#### **Exploratory Data Analysis (EDA)**
* **Descriptive Statistics:** We computed and visualized descriptive statistics to uncover **booking patterns**. This included analyzing cancellation rates, distribution of lead times, and average pricing behaviors across different booking segments.
* **Cancellation Drivers:** A key focus of the EDA was to understand the factors influencing cancellations. Our analysis highlighted that cancellation patterns are strongly influenced by **booking lead time** and **room type**, with longer lead times and certain room types showing higher cancellation rates.

---

### **🛠️ Tech Stack**

* **Language:** Python
* **Libraries:**
    * **Data Handling:** `pandas`, `numpy`
    * **Visualization:** `matplotlib`, `seaborn`, `missingno`
    * **Utilities:** `warnings`

---

### **📊 Insights**

* The dataset contains notable **outliers** in pricing (`adr`) and booking lead times, which require careful handling before model training.
* Missing values are predominantly concentrated in specific categorical features, particularly `agent` and `company`.
* **Cancellation patterns** are highly correlated with **booking lead time** and **room type**, suggesting these are critical features for a predictive model.
