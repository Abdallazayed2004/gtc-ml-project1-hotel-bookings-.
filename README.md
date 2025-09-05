📊 Hotel Booking Demand Analysis
Overview

This project explores and analyzes the Hotel Booking Demand dataset to uncover patterns in customer reservations, cancellations, and booking behavior. The goal is to perform data cleaning, exploratory data analysis (EDA), and preprocessing to prepare the dataset for further machine learning modeling.

Dataset

Source: Hotel Booking Demand dataset (Kaggle)

Shape: ~119k rows × 32 columns

Description: Contains information about hotel bookings such as booking dates, length of stay, number of guests, meal plans, country of origin, deposit type, and whether a booking was canceled.

Project Workflow

Data Loading & Inspection

Imported CSV file using pandas

Examined structure, data types, and summary statistics

Data Cleaning

Identified missing values using missingno and heatmaps

Checked and removed duplicate rows

Handled null values appropriately

Outlier Detection

Applied IQR method to detect outliers in numerical features (adr, lead_time)

Visualized distributions with boxplots

Exploratory Data Analysis (EDA)

Heatmaps for missing data

Statistical summaries

Initial visualizations to highlight booking trends

Tools & Libraries

Python

Pandas, NumPy

Matplotlib, Seaborn

Missingno

Results & Insights

Dataset contained significant missing values in certain features

Outliers detected in adr (Average Daily Rate) and lead_time

Preprocessed dataset is ready for further machine learning tasks such as predicting cancellations or customer segmentation

Usage

Clone the repository and open the notebook:

git clone https://github.com/yourusername/hotel-booking-analysis.git
cd hotel-booking-analysis
jupyter notebook gtc_ml_project1_hotel_bookings__.ipynb

Future Work

Feature engineering for categorical variables

Building predictive models (Decision Trees, Random Forest, SVM)

Model evaluation & hyperparameter tuning

Repository Structure
├── gtc_ml_project1_hotel_bookings__.ipynb   # Main notebook
├── hotel_bookings.csv                       # Dataset (if included)
├── README.md                                # Project documentation
└── requirements.txt                         # Python dependencies

Author

Your Name
Project completed as part of a machine learning coursework project.
