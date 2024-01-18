# Sales Insights Data Analysis Project

# Project overview

This data analysis project aims to provide insights into the sales performance of an e-commerce company over the past year. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's performance.

### Data source

Sales Data: the primary dataset used for this analysis is "db_dump" file containing details about each sale made by the company.

### Tools

- MySQL- Data analysis 
- Power BI- Creating reports
    - [download here](https://powerbi.microsoft.com/en-us/downloads/)

### Data cleaning/preparation

In the initial data preparation phase, we perforned the following tasks:
1. Data Loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.

### Exploratory Data Analysis

EDA involves exploring sales data to anser key questions, such as:

- What is the overall sales trend ?
- Which products are top sellers ?
- What are the peak sales period ?

### Data Analysis

Include some interesting code/features Using SQL


1. Show all customer records

    SELECT * FROM customers;

2. Show total number of customers

    SELECT count(*) FROM customers;

3. Show transactions for Chennai market ,market code for chennai is Mark001

    SELECT * FROM transactions where market_code='Mark001';

4. Show distinct product codes that were sold in chennai

    SELECT distinct product_code FROM transactions where market_code='Mark001';

5. Show transactions where currency is US dollars

    SELECT * from transactions where currency="USD"

6. Show transactions in 2020 join by date table

    'SELECT transactions.date FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;'

7. Show total revenue in year 2020

    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";
	
8. Show total revenue in year 2020, January Month

    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9. Show total revenue in year 2020 in Chennai

    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";




