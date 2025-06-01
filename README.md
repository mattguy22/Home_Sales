# **SparkSQL Challenge: Home Sales Data Analysis Project**

Created by Matthew Guy, 2025

A data analysis project using **Apache Spark and PySpark SQL**. This project analyzes a home sales dataset by creating Spark DataFrames, running complex SQL queries, caching data, partitioning, and measuring performance. The analysis provides insights into average home prices based on bedrooms, bathrooms, floors, square footage, and view ratings.

---

## **Table of Contents**
- [Features](#features)
- [Installation](#installation)
- [Usage Instructions](#usage-instructions)
- [Dataset Details](#dataset-details)
- [Analysis Functionality](#analysis-functionality)
- [Sample Outputs](#sample-outputs)
- [Deployment](#deployment)
- [Future Enhancements](#future-enhancements)
- [About](#about)
- [Resources](#resources)

---

## **Features**

**SparkSQL Analysis**: Queries executed using SparkSQL for performance and scalability.  
**Data Partitioning**: Parquet file generation with partitioning by `date_built`.  
**Caching/Uncaching**: Temporarily cache a SparkSQL table to improve query performance.  
**SQL Queries**: Calculate average home prices based on various criteria, including bedrooms, bathrooms, and view ratings.  
**Performance Measurement**: Compare query runtimes on uncached, cached, and partitioned data.  

---

## **Installation**

### **Requirements**
- GitHub Account  
- VS Code or Jupyter Notebook  
- Python and PySpark installed

### **Quick Start Setup**

1. Clone or download the repository.  
2. Open the `Home_Sales` project in VS Code or Jupyter.  
3. Ensure files are in the correct structure:

&nbsp;&nbsp;&nbsp;&nbsp;📁 HOME_SALES  
&nbsp;&nbsp;&nbsp;&nbsp;├── 📁 Completed Script  
&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;└── 📄 home_sales_partitioned.parquet  
&nbsp;&nbsp;&nbsp;&nbsp;├── 📄 Home_Sales.ipynb  
&nbsp;&nbsp;&nbsp;&nbsp;└── 📄 README.md  

4. Run the `Home_Sales.ipynb` notebook.  
5. Review query outputs and runtime comparisons.

---

## **Usage Instructions**

- Open `Home_Sales.ipynb` in Jupyter or VS Code.  
- Execute each cell step-by-step to read the dataset, create tables, and run SparkSQL queries.  
- Observe outputs for average prices per year, partitioned data, and view rating analysis.  
- Note runtime comparisons between uncached, cached, and partitioned queries.

---

## **Dataset Details**

- **Source**: Provided in AWS S3 (linked in the notebook).  
- **Data Includes**: Home ID, sale date, date built, price, bedrooms, bathrooms, living area, lot size, floors, waterfront presence, and view rating.  
- Data is loaded into a Spark DataFrame and processed with SparkSQL.

---

## **Analysis Functionality**

- **SparkSQL** executes complex SQL queries to calculate average home prices:  
  - Per year for four-bedroom houses  
  - Per year for homes with 3 beds, 3 baths  
  - Per year for homes with 3 beds, 3 baths, 2 floors, and ≥ 2000 sqft  
  - Per view rating for homes with average price ≥ $350,000  
- **Caching**: Temporarily caches the home sales table to improve query performance.  
- **Partitioning**: Saves data partitioned by `date_built` in Parquet format and re-queries it.  

---

## **Sample Outputs**

### Average Price by Bedrooms and Year
Results showing average home prices for four-bedroom houses, rounded to two decimal places.

### Average Price by View Rating
Query outputs average price per view rating for homes with average price ≥ $350,000, showing runtime comparisons.

---

## **Deployment**

To run this project locally:

1. Clone or download the `Home_Sales` repository.  
2. Open the `Home_Sales.ipynb` notebook in Jupyter or VS Code.  
3. Step through each cell sequentially to perform the analysis.  
4. Optionally push updates to your GitHub repository for submission.

---

## **Future Enhancements**

- Add more complex queries using window functions or joins  
- Automate generation of summary reports and charts  
- Explore dataset augmentation with additional property details  

---

## **About**

This project was built as part of the Module 22 Challenge. It demonstrates skills in big data processing, SparkSQL querying, performance tuning, and PySpark-based data analysis.

---

## **Resources**

- [Apache Spark Documentation](https://spark.apache.org/docs/latest/)  
- [PySpark SQL Documentation](https://spark.apache.org/docs/latest/sql-programming-guide.html)  
- [Jupyter Notebooks](https://jupyter.org/)  
- [AWS S3 Data Link (provided in notebook)]  
- **DU Bootcamp Module 22**: Used for Spark, SQL, and data partitioning examples.  
- **ChatGPT**: Assisted with SQL syntax, partitioning, and caching implementation guidance.
