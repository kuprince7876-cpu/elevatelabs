# Data Cleaning & Preprocessing – Titanic Dataset

## Overview

This project focuses on **data cleaning and preprocessing of the Titanic dataset** as part of Task 1 of the AI & ML Internship. The main purpose of this task was to understand how raw and incomplete data can be cleaned and transformed into a suitable format for Machine Learning.

## Objective

The objective of this task is to learn and apply different data preprocessing techniques, including handling missing values, converting categorical data, scaling numerical features, detecting outliers, and preparing the final dataset for Machine Learning.

## Tools and Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## Steps Performed

The Titanic dataset was first imported and examined to understand its structure, data types, and missing values. Missing values were then handled according to the type of data. The missing values in the **Age** column were replaced with the median value, while categorical columns such as **Embarked, Deck, and Embark_Town** were filled using their respective mode values.

Categorical variables were converted into numerical form using **one-hot encoding** with `pd.get_dummies()` and `drop_first=True`. After that, numerical features were standardized using **StandardScaler**, which transforms the data to have a mean of zero and a standard deviation of one.

Outliers were identified using **boxplots** and the **Interquartile Range (IQR) method**. Values outside the range of **Q1 − 1.5 × IQR** and **Q3 + 1.5 × IQR** were considered outliers and removed from the dataset.

## Files Included

* **preprocessing.py** – Python script containing the complete preprocessing process.
* **titanic_original.csv** – Original Titanic dataset used for the project.
* **titanic_processed.csv** – Final cleaned and preprocessed dataset.
* **outlier_boxplots.png** – Boxplot visualization showing the data before and after outlier removal for the Fare column.

## Key Learnings

Through this task, I learned how different types of missing data, such as **MCAR, MAR, and MNAR**, can affect a dataset. I also understood the difference between **Label Encoding and One-Hot Encoding** and when they are used.

The project also helped me understand the difference between **Normalization (Min-Max Scaling)** and **Standardization (Z-score Scaling)**. In addition, I learned how boxplots, the IQR method, and Z-score can be used to identify outliers.

Most importantly, this task showed how proper preprocessing can make data more suitable for Machine Learning by handling missing values, reducing unwanted variations, and potentially improving model performance. However, preprocessing techniques must be selected carefully because inappropriate data cleaning can also affect the accuracy of a model.

## How to Run the Project

Make sure that **Python 3.x** is installed on your system. Install the required libraries using:

`pip install pandas numpy matplotlib seaborn scikit-learn`

After installing the dependencies, run the preprocessing script:

`python3 preprocessing.py`

The processed dataset will be generated and saved as **titanic_processed.csv**.

## Results

* **Original dataset:** 891 rows × 15 columns
* **Processed dataset:** 598 rows × 24 columns
* **Rows removed:** 293

A total of **293 rows were removed as outliers** based on the IQR method applied to the numerical features. The final dataset contains cleaned, encoded, and standardized data that can be used for further Machine Learning tasks.
