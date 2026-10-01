# 🎬 Movie Sales Dashboard – Cinema Sales Analysis

An interactive Power BI dashboard designed to analyze cinema movie sales, transactions, revenue, payment methods, sales channels, movie performance, and transaction status.

This project demonstrates how transactional cinema data can be transformed into an interactive dashboard to monitor sales performance and generate business insights.

---

## 📌 Project Overview

The **Movie Sales Dashboard** is a data analytics project built using **Microsoft Power BI**.

The dashboard analyzes cinema transaction data from different perspectives, including sales performance, movie performance, customer transactions, payment methods, sales channels, studio usage, and transaction status.

The project focuses on transforming raw transaction data into meaningful visual insights that can support business monitoring and decision-making.

### Main questions addressed in this project:

- How are cinema transactions performing over time?
- How much revenue is generated from ticket sales?
- Which movies generate the highest revenue?
- Which genres contribute the most to sales?
- What is the distribution of transaction status?
- Which payment methods are most frequently used?
- Which sales channels generate the most transactions?
- How are transactions distributed across studios?
- How does auditorium type relate to transactions?
- What are the characteristics of individual transactions?

---

## 🎯 Project Objectives

The main objectives of this project are:

1. Monitor overall cinema sales and transaction performance.
2. Analyze revenue and ticket sales trends.
3. Identify movies and genres with strong sales performance.
4. Understand customer transaction behavior.
5. Analyze the usage of payment methods and sales channels.
6. Monitor transaction status and completion rate.
7. Provide an interactive dashboard for business performance monitoring.

---

## 🗂️ Dataset

The main transactional dataset used in this project is **Data Final**.

The dataset contains information related to cinema transactions, movie information, customers, payment methods, sales channels, studios, seats, and ticket purchases.

### Main fields in the transaction dataset

| Category | Fields |
|---|---|
| Transaction | `order_id`, `transaction_date`, `transaction_time` |
| Movie | `Movie ID`, `Movie Title`, `Genre`, `Rating` |
| Show | `show_date`, `show_time`, `studio_number`, `auditorium_type`, `seat_number` |
| Customer | `customer_name` |
| Sales | `quantity`, `ticket_price`, `subtotal`, `total_payment` |
| Payment | `payment_method` |
| Channel | `channel` |
| Combo | `combo_name`, `combo_price`, `combo_addon` |
| Status | `status` |
| Source | `Source.Name` |
| Time Category | `day_category` |

---

## 🧹 Data Preparation

The data was prepared in Power BI before being used for dashboard development.

The preparation process includes:

1. Reviewing the available fields and data structure.
2. Organizing transaction and reference data.
3. Connecting the transaction table with movie, channel, and payment mapping tables.
4. Establishing relationships between the tables.
5. Preparing numerical fields for aggregation.
6. Creating the necessary calculations and measures for dashboard KPIs.
7. Designing interactive visualizations based on the business questions.

---
📊 Dashboard

The dashboard provides an interactive overview of cinema sales performance.

Dashboard Preview
