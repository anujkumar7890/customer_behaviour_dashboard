# Customer Shopping Behavior Analysis

## Overview

This project analyzes customer shopping behavior for a retail company to uncover trends, identify purchase drivers, improve customer engagement, and support data-driven business decisions. The analysis combines **Python for data preparation**, **SQL for data modeling and querying**, and **Power BI for interactive visualization**.

The project addresses the business question:

> *How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?* 

---

## Business Objectives

* Understand customer purchasing patterns across demographics.
* Identify factors influencing buying decisions.
* Analyze the impact of discounts, reviews, and promotional activities.
* Segment customers based on age and purchasing behavior.
* Compare customer preferences across product categories and sales channels.
* Generate actionable insights for marketing, sales, and product strategy. 

---

## Project Structure


Customer-Shopping-Behavior-Analysis/
│
├── Customer_Shopping_Behavior_Analysis.ipynb    # Data cleaning & transformation
├── customer_behavior_dashboard.pbix            # Power BI dashboard
├── SQL/
│   ├── schema.sql
│   ├── data_model.sql
│   └── analysis_queries.sql
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── reports/
│   ├── Project_Report.pdf
│   └── Presentation.pptx
│
└── README.md


## Technologies Used

### Data Preparation & Analysis

* Python
* Pandas
* NumPy

### Database

* PostgreSQL
* MySQL
* Microsoft SQL Server
* SQLAlchemy

### Visualization

* Power BI

---

## Dataset Features

The dataset contains customer shopping information including:

* Customer demographics (Age, Gender)
* Product categories
* Purchase amount
* Review ratings
* Discount usage
* Purchase frequency
* Payment methods
* Seasonal purchasing trends
* Shopping preferences

---

## Data Preparation

The notebook performs the following preprocessing steps:

### 1. Data Exploration

* Load dataset using Pandas
* Inspect data structure
* Generate summary statistics
* Check for missing values

### 2. Missing Value Treatment

* Missing values in **Review Rating** are imputed using the median rating within each product category.

### 3. Data Standardization

* Convert column names to **snake_case** format.
* Rename inconsistent column names for better readability.

### 4. Feature Engineering

#### Age Group Creation

Customers are segmented into:

* Young Adult
* Adult
* Middle-aged
* Senior

using quartile-based age grouping.

#### Purchase Frequency Conversion

Categorical purchase frequencies are converted into numerical days:

| Frequency   | Days |
| ----------- | ---- |
| Weekly      | 7    |
| Bi-Weekly   | 14   |
| Fortnightly | 14   |
| Monthly     | 30   |
| Quarterly   | 90   |
| Annually    | 365  |

### 5. Data Cleaning

* Validate duplicate information between discount and promo code fields.
* Remove redundant columns.

---

## Database Integration

The notebook includes examples for exporting the cleaned dataset into:

### PostgreSQL

python
from sqlalchemy import create_engine

engine = create_engine(
    "postgresql://username:password@localhost:5432/customer_behavior"
)

df.to_sql("customer_behavior", engine, if_exists="replace")


### MySQL

python
engine = create_engine(
    "mysql+pymysql://username:password@localhost:3306/customer_behavior"
)

### Microsoft SQL Server

python
engine = create_engine(
    "mssql+pyodbc://..."
)


## SQL Analysis Goals

Example business questions:

* Which customer segments generate the highest revenue?
* How does discount usage affect purchasing behavior?
* Which product categories receive the highest ratings?
* What payment methods are most preferred?
* Which seasons produce the highest sales?
* Which customer groups demonstrate higher purchase frequency?

---

## Power BI Dashboard

The Power BI dashboard provides interactive insights into:

### Customer Insights

* Age distribution
* Gender breakdown
* Customer segments

### Sales Performance

* Revenue trends
* Product category performance
* Seasonal sales analysis

### Purchase Behavior

* Purchase frequency analysis
* Discount utilization
* Review rating impact

### Payment & Shopping Preferences

* Preferred payment methods
* Online vs. offline shopping patterns

---

## Key Business Insights

Potential insights generated from the analysis include:

* High-value customer segments.
* Most profitable product categories.
* Impact of discounts on purchasing decisions.
* Relationship between customer reviews and sales.
* Seasonal demand fluctuations.
* Preferred payment channels and shopping methods.

---

## Business Recommendations

### Marketing

* Target promotions to high-value customer segments.
* Personalize campaigns using demographic insights.

### Product Strategy

* Increase focus on high-performing categories.
* Improve underperforming products through customer feedback analysis.

### Customer Retention

* Reward frequent buyers through loyalty programs.
* Use review data to improve customer satisfaction.

### Pricing & Promotions

* Optimize discount strategies based on customer responsiveness.
* Monitor promotional effectiveness across segments.

---

## How to Run the Project

### 1. Clone Repository

git clone https://github.com/anujkumar7890/customer_behaviour_dashboard.git
cd customer-shopping-behavior-analysis

### 2. Install Dependencies

pip install pandas numpy sqlalchemy psycopg2-binary pymysql pyodbc

### 3. Run Notebook

jupyter notebook Customer_Shopping_Behavior_Analysis.ipynb

### 4. Open Power BI Dashboard

Open:

customer_behavior_dashboard.pbix


using Power BI Desktop.


## Deliverables

* Data Cleaning & Transformation (Python)
* Database Modeling & Analysis (SQL)
* Interactive Dashboard (Power BI)
* Business Insights & Recommendations
* GitHub Repository Documentation 

---

## Author-Anuj Kumar Prajapati

**Customer Shopping Behavior Analysis Project**

A retail analytics project focused on understanding customer purchasing behavior and enabling data-driven decision-making.
