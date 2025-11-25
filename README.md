📊 Task 1 – Exploratory Data Analysis (EDA)

This repository contains my work for Task 1 of the GDG Data Science Committee, completed in Google Colab.
The task focuses on performing Exploratory Data Analysis (EDA) on a given dataset using Python.

🔍 Overview

The objective of this task is to understand and implement the key concepts of EDA, including:

Data inspection

Data cleaning

Handling missing/invalid values

Feature encoding

Normalization & Standardization

Basic visualizations

Automated profiling

This task helped in understanding how raw data is transformed into clean, structured, and meaningful information suitable for machine learning.

🧰 Tools & Libraries Used

Python

Pandas – Data manipulation

NumPy – Numerical operations

Matplotlib / Seaborn – Data visualization

ydata-profiling – Automated data profiling

scikit-learn – Encoding & scaling

📝 Key Steps Performed
1. Mounting Google Drive

Loaded dataset directly from Google Drive:

from google.colab import drive
drive.mount('/content/drive')

2. Installing Required Libraries
!pip install ydata-profiling -q

3. Loading the Dataset
df = pd.read_csv('/content/drive/MyDrive/.../crab_age.csv')

4. Data Cleaning

Removed rows where Height = 0

Reset index after dropping rows

Verified dataset shape: (74027, 9)

df = df[df['Height'] != 0]
df.reset_index(drop=True, inplace=True)

5. Handling Categorical Data

Performed One Hot Encoding on the Sex column:

df = pd.get_dummies(df, columns=['Sex'], drop_first=True)

6. Feature Scaling

Applied both:

✔ Normalization (Min-Max Scaling)
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
df_normalized = df.copy()
df_normalized[num_cols] = scaler.fit_transform(df[num_cols])

✔ Standardization (Z-Score)
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
df_standardized = df.copy()
df_standardized[num_cols] = scaler.fit_transform(df[num_cols])

7. Automated EDA Report

Generated a complete profiling report:

from ydata_profiling import ProfileReport
profile = ProfileReport(df)
profile.to_file("EDA_report.html")

📁 Files in this Repository

Task1_EDA.ipynb – Main notebook

EDA_report.html – Automated profiling report

README.md – Explanation of the task

🚀 What I Learned

How to explore a new dataset systematically

Importance of cleaning incorrect values

Encoding techniques (One-Hot vs Label Encoding)

How scaling affects different features

How to generate quick EDA reports

Improved Python + pandas proficiency

📌 Future Improvements

Add more visualizations

Try feature engineering

Train a simple ML model using cleaned data
