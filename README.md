# End-to-End-Machine-Learning-on-Amazon-Shoe-Data---Python-MySQL-ML-Tools

An end-to-end Data Science and Machine Learning capstone project that focuses on scraping, analyzing, clustering, and classifying Amazon e-commerce shoe data. The project involves data engineering, unsupervised and supervised ML models, and ends with storing structured results in a MySQL database.

# 📌 Project Overview

This project analyzes e-commerce shoe data scraped from Amazon using Selenium and BeautifulSoup. The goal is to:

* Perform exploratory data analysis (EDA)

* Group products into pricing segments (Low, Medium, Premium) using clustering

* Predict shoe categories using classification algorithms

* Store the final structured data in a MySQL database for future usage

# 🎯 Objectives

* 🔍 Scrape Amazon shoe data with dynamic content handling

* 🧹 Clean and preprocess the data

* 📊 Perform EDA to extract insights

🧠 Apply Unsupervised Learning using KMeans clustering

* 🤖 Apply Supervised Learning using models like:

---Logistic Regression

---K-Nearest Neighbors (KNN)

---Support Vector Machines (SVM)

---Random Forest

---XGBoost

* ⚖️ Use SMOTE to address class imbalance

* 🧪 Evaluate models using accuracy and F1-score

* 🗄️ Store final output in MySQL database

# 🛠️ Tools & Libraries Used

Purpose	Tools / Libraries
Web Scraping	Selenium, BeautifulSoup
Data Manipulation	Pandas, NumPy
Visualization	Matplotlib, Seaborn
Machine Learning	Scikit-learn, XGBoost
Data Storage	MySQL
Class Balancing	imblearn.SMOTE

# 📊 Data Overview

* Source: Amazon Shoe Listings

* Collected Features:

--- Brand

--- Product Title

--- User Rating

--- Price

* New Feature Created:

--- Category: Derived from product title (e.g., Sneakers, Walking, Running)

# 🔍 Exploratory Data Analysis (EDA)

* Handled missing values and duplicates

* Converted rating to float format

* Extracted shoe types from titles

* Identified skewed distribution in price

* No significant correlation between price and rating

* Most products fall in ₹500–₹3000 range

# 🔄 Unsupervised Learning – Clustering

* Used KMeans Clustering (n_clusters=3) based on price and rating:

* Cluster	Description
--- 0	Mid-price, high rating (₹1500–₹6000)
--- 1	Budget, high rating (< ₹3000)
--- 2	Premium, moderate-to-high rating

* Validated using the Elbow Method

* Visualized with scatter plots

# 🤖 Supervised Learning – Classification

* Applied multiple ML models and tuned them with SMOTE:

Model	Train Accuracy	Test Accuracy	Notes
Logistic Regression	99%	99%	Stable across datasets
SVM	100%	96–98%	Great generalization
KNN	100%	~94%	Sensitive to class sizes
Random Forest	100%	98%	Excellent with SMOTE
XGBoost	100%	98%	✅ Final model (best F1)

✅ Final Model: XGBoost with SMOTE and hyperparameter tuning

# 🗄️ Data Storage – MySQL

Created shoes schema and table in MySQL Workbench

Used .csv import via Table Data Import Wizard

Stored cleaned and labeled dataset for persistence

# ✅ Key Outcomes

📌 End-to-End ML Pipeline: Scraping → EDA → Modeling → Deployment

🧠 Uncovered 3 price-based product segments

🏆 XGBoost chosen as the final classification model with 98% accuracy

💾 MySQL used for structured data storage

# 🔚 Conclusion

This capstone demonstrates the complete lifecycle of a real-world ML project — from raw web scraping to final deployment-ready insights. It reflects the integration of multiple skills: data engineering, analytics, ML modeling, and database systems.

