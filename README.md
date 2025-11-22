# Customer-data-analysis
📊 Customer Data Analysis — README
📁 Project Overview

This project analyzes customer shopping behavior across 10 malls in Istanbul (2021–2023).
Using SQL Server and Power BI, it identifies revenue-driving segments, category trends, and payment-method insights.
The repository contains the SQL documentation, Power BI dashboard, and presentation slides.

📂 Repository Structure
/Customer-Data-Analysis
│── Customer Data Analysis ppt.pptx
│── SQL CUSTOMER SEGEMENT PROJECT.docx
│── project customer segmentation.pbix
│── README.md

🎯 Key Objectives

Identify top revenue-generating age groups and genders

Understand category preferences (Clothing, Electronics, Cosmetics, etc.)

Analyze payment method behavior (Cash, Credit Card, Debit Card)

Compare performance across shopping malls

Provide data-driven recommendations to improve revenue and engagement

🗂️ Dataset Summary

Years Covered: 2021–2023

Fields Included:
invoice_no, customer_id, gender, age, category, quantity, price, payment_method, invoice_date, shopping_mall

🧹 Data Cleaning (SQL Server)

The following preprocessing steps were performed:

Removed duplicate records

Standardized gender, category, and payment method values

Converted invoice dates to valid date formats

Validated price and quantity fields

Created age groups for segmentation

Full SQL documentation is in:
📄 SQL CUSTOMER SEGEMENT PROJECT.docx (/mnt/data/SQL CUSTOMER SEGEMENT PROJECT.docx)

📶 Analysis Highlights

Females contribute the highest revenue and transaction volume

Age group 20–30 is the top spending segment

Clothing is the most purchased category overall

Cash is still the dominant payment method, but card usage is higher among younger customers

Mall of Istanbul is the top mall in revenue

📊 Dashboard

An interactive Power BI dashboard visualizes:

Customer segmentation

Category-wise revenue

Age & gender distributions

Mall-wise comparison

Payment method trends

📁 Open the dashboard:
project customer segmentation.pbix (/mnt/data/project customer segmentation.pbix)

🧩 Sample SQL Queries

1. Gender-wise transactions

SELECT gender, COUNT(*) AS total_transactions
FROM customer
GROUP BY gender;


2. Total revenue by age group

SELECT 
  CASE 
    WHEN age < 20 THEN 'Below 20'
    WHEN age BETWEEN 20 AND 30 THEN '20-30'
    WHEN age BETWEEN 31 AND 40 THEN '31-40'
    WHEN age BETWEEN 41 AND 50 THEN '41-50'
    ELSE '50+'
  END AS age_group,
  SUM(price * quantity) AS total_revenue
FROM customer
GROUP BY age_group;

💡 Business Recommendations

Launch targeted marketing campaigns for the 20–30 age group

Improve offers for underperforming categories like kids books & electronics

Promote digital payment adoption via loyalty rewards

Create female-focused clothing and cosmetics bundles

Use data insights to plan mall-specific promotional events

🛠️ Tools Used

SQL Server — Data cleaning, transformations & analysis

Power BI — Visualization & dashboard development

PowerPoint — Presentation documentation

🚀 How to Use This Repository

Open SQL documentation (SQL CUSTOMER SEGEMENT PROJECT.docx) to review cleaning logic and queries

Load the cleaned dataset into Power BI

Open the .pbix file to explore visual insights

Review the presentation file to understand findings and recommendations
