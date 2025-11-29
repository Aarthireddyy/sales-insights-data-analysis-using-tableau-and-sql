<h1 align="center">Sales Insights - Data Analysis using Tableau and SQL</h1>

This repository provides a comprehensive analysis of sales for an India-based hardware company. The project utilizes Tableau and SQL to extract insights and visualize key performance indicators to support data-driven business decisions.

### About Project

- Performed a detailed sales insights analysis for a hardware company based in India.
- Developed ETL mappings using SQL to extract data from unstructured sources and transformed it into a staging area for data cleaning.
- Designed a star schema data model within Tableau to facilitate efficient analysis.
- Developed a Tableau dashboard to perform quantitative visualizations, drawing insights based on various parameters affecting company performance year-over-year.
- Provided actionable business solutions based on the data findings.

## Technologies Used

- Advanced Excel: Used for initial data exploration and supplementary visualization.
- MySQL / SQL Server: Utilized for data storage, ETL processes, and complex querying.
- Tableau / Power BI: Employed for data modeling and creating interactive dashboards.
- Statistics: Applied statistical methods to ensure data accuracy and meaningful insights.

## Certifications and Project Foundation

The methodology for this project is supported by industry-standard practices and certifications, including:

- Data Visualization with Tableau - Simplilearn
- Databases and SQL for Data Science with Python - IBM
- Statistics for Data Science with Python - IBM
- Data Visualization with Advanced Excel - PWC

## Project - India based Hardware company Sales Insights

### Tableau Dashboard Link
[Tableau Dashboard: Revenue Analysis](https://public.tableau.com/views/SalesInsights-DataAnalysisProject/Dashboard-RevenueAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link)

### Problem Statements
The Sales Director requires visibility into the performance of the company across various Indian states to optimize discount strategies and revenue growth.

- Q1. Revenue breakdown by cities.
- Q2. Revenue breakdown by years and months.
- Q3. Top 5 customers by revenue and sales quantity.
- Q4. Top 5 Products by revenue.
- Q5. Net Profit and Profit Margin by Market.

### Approach - Project Planning and Aims Grid

#### 1. Purpose
To unlock sales insights that were previously unavailable to the sales team, providing decision support and automating manual data gathering processes.

#### 2. Stakeholders
- Sales Director
- I.T. Team
- Customer Service Team
- Data and Analytics Team

#### 3. End Result
An automated dashboard providing quick and current sales insights to support data-driven decision making.

#### 4. Success Criteria
- Dashboards uncovering sales order insights with the latest available data.
- Sales team enabled to make better decisions, targeting a 10% cost saving of total spend.
- Sales analysts saving 20% of their time by eliminating manual data gathering.

### Data Analysis - Approach
The project follows a structured flow: Data Discovery -> Data Cleaning -> Data Transformation -> Data Visualization -> Insight Generation.

### Setup Process

Step 1: Download the database files: db_dump.sql or db_dump.xlsx.

Step 2: Import the data into MySQL and perform ETL (Extract, Transform, Load) as required.

Step 3: Utilize Tableau Public or Tableau Desktop to perform the Data Analysis.

Step 4: Connect Tableau to the MySQL database or Excel source.

Step 5: Save the analysis file in .twb or .twbx format.

## Data Analysis Using SQL

1. Show all customer records:
   SELECT * FROM customers;

2. Show total number of customers:
   SELECT count(*) FROM customers;

3. Show transactions for Chennai market (market code for Chennai is Mark001):
   SELECT * FROM transactions where market_code='Mark001';

4. Show distinct product codes that were sold in Chennai:
   SELECT distinct product_code FROM transactions where market_code='Mark001';

5. Show transactions where currency is US dollars:
   SELECT * from transactions where currency="USD";

6. Show transactions in 2020 joined by date table:
   SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7. Show total revenue in year 2020:
   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

8. Show total revenue in year 2020, January Month:
   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9. Show total revenue in year 2020 in Chennai:
   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

## Data Analysis Using Tableau

### Tableau Public Dashboards: Revenue and Profit Analysis
The dashboards provide an interactive interface to explore revenue trends and profit margins across different regions and timeframes.

#### Creating Star Schema in Tableau
The data model is structured using a Star Schema, connecting fact tables with dimension tables (customers, products, markets, and date) to optimize query performance and reporting.

#### Tableau Dashboard - Revenue Analysis
This view focuses on top-line growth, identifying key markets and products contributing to the company's revenue.

#### Tableau Dashboard - Profit Analysis
This view analyzes the bottom line, highlighting profit margins and identifying areas where cost-to-revenue ratios can be improved.

## Project References

1. Tableau Project Dashboard: Sales Insights - Data Analysis using Tableau
2. Tableau Public Profile: Data Analysis Portfolio
3. Tutorial: Sales Insights Data Analysis Series
4. MySQL Installation Guide
5. OLTP and OLAP: Differences and Use Cases
6. Star Schema: Fact Table and Dimension Table Documentation

## Related Projects

- Spotify Data Analysis using Python
- Statistics for Data Science using Python
- Python Lessons for Data Analysis
- Python Libraries for Data Science

## Maintainer

### Aarthi Reddy Jannapureddy
Aarthi Reddy Jannapureddy is a Data Analyst with over 3 years of experience specializing in SQL, Power BI, Tableau, and Python. She has a proven track record of building robust reporting systems and dashboards that improve data accuracy and support strategic business decisions. Her expertise spans retail and enterprise environments, focusing on KPI tracking, forecasting, and process automation.

- LinkedIn: https://www.linkedin.com/in/aarthireddyj
- Email: aarthireddyj@gmail.com
- GitHub: https://github.com/aarthireddyj