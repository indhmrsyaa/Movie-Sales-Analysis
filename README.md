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

## 🏗️ Data Model

The Power BI data model consists of one main transaction table and several supporting dimension/mapping tables.

### Main Table

**Data Final**

This table contains the detailed cinema transaction records and acts as the central table for analysis.

### Supporting Tables

**Movie Master**

Contains movie-related information such as:

- Movie ID
- Movie Title
- Genre
- Rating

**Channel_Mapping_Cinema**

Used to map cinema sales channels into their corresponding channel categories.

Fields:

- `channel`
- `Channel_Mapping`

**Payment_Mapping_Cinema**

Used to standardize or categorize payment methods.

Fields:

- `payment_method`
- `Payment_Mapping`

### Data Model Structure

```text
                    ┌─────────────────────┐
                    │     Movie Master    │
                    │─────────────────────│
                    │ Movie ID            │
                    │ Movie Title         │
                    │ Genre               │
                    │ Rating              │
                    └──────────┬──────────┘
                               │
                               │ 1 : *
                               ▼
                    ┌─────────────────────┐
                    │      Data Final     │
                    │─────────────────────│
                    │ order_id            │
                    │ Movie ID            │
                    │ Movie Title         │
                    │ Genre               │
                    │ quantity            │
                    │ ticket_price        │
                    │ subtotal            │
                    │ total_payment       │
                    │ payment_method      │
                    │ channel             │
                    │ status              │
                    │ show_date           │
                    │ show_time           │
                    │ ...                 │
                    └─────────┬───────────┘
                              │
                 ┌────────────┴────────────┐
                 │                         │
                 ▼                         ▼
      ┌─────────────────────┐   ┌─────────────────────┐
      │ Channel Mapping     │   │ Payment Mapping     │
      │─────────────────────│   │─────────────────────│
      │ channel             │   │ payment_method      │
      │ Channel_Mapping     │   │ Payment_Mapping     │
      └─────────────────────┘   └─────────────────────┘
