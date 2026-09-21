# E-Commerce Sales, Customer & Product Analytics

## Project Overview
This project analyzes e-commerce sales, customer, product, order, and payment data using Microsoft Power BI.

The dashboard provides a business-focused view of sales performance, customer behaviour, product and category performance, order status, payment methods, and customer value and retention.

## Project Objectives
- Analyze sales and revenue performance
- Understand customer purchasing behaviour
- Identify high-performing products and categories
- Analyze orders, delivery, and cancellations
- Understand payment method performance
- Analyze customer value and retention
- Generate business insights and recommendations

## Dataset
The project uses four main tables:
- **Customers** — customer profile and registration information
- **Products** — product details, categories, prices, and stock
- **Orders** — order-level information
- **Order Items** — products purchased within each order

A separate **DateTable** was created for time-based analysis.

## Data Cleaning & Preparation
Data preparation was performed using **Power Query**.

Key validation checks included:
- Missing IDs and values
- Duplicate records
- Blank customer/product names
- Inconsistent cities and categories
- Invalid dates
- Invalid or missing prices
- Missing, zero, or negative stock
- Missing/orphan customer IDs in orders
- Invalid order and product IDs in order items
- Quantity and unit-price validation

## Data Model
```text
Customers → Orders → Order Items ← Products
                    ↑
                 DateTable
```

An inactive relationship between `DateTable[Date]` and `Customers[signup_date]` was created for customer signup analysis.

## DAX Analysis
Important measures and calculations include:
- Total Revenue
- Total Orders
- Average Order Value
- Total Quantity Sold
- Revenue Growth %
- Total Customers
- New Customers
- Repeat Customers
- Customer Repeat Rate %
- Revenue per Customer
- Average Orders per Customer
- Delivered Orders
- Cancelled Orders
- Cancellation Rate
- Delivery Rate
- Top Product by Revenue
- Top Category by Revenue

Customer segmentation was also created using purchase behaviour and revenue.

## Dashboard Pages

### 1. Sales Performance
- Total Revenue
- Total Orders
- Average Order Value
- Total Quantity Sold
- Monthly Revenue Trend
- Revenue by Category
- Top 10 Products by Revenue
- Revenue by City
- Quantity Sold by Category
- Product Revenue vs Quantity
- Monthly Revenue Growth

### 2. Customer Analytics
- Total Customers
- New Customers
- Repeat Customers
- Average Revenue per Customer
- Customer Distribution by City
- Customer Revenue by City
- Customer Signup Trend
- Customer Segmentation
- Top 10 Customers by Revenue
- Customer Revenue by Type

### 3. Product & Category
- Total Products Sold
- Average Product Price
- Product Quantity Sold
- Top Category by Revenue
- Revenue by Category
- Quantity Sold by Category
- Top and Bottom Products by Quantity
- Stock Status
- Product Price vs Quantity Sold
- Category Revenue Contribution
- Average Price by Category

### 4. Orders & Payment
- Total Orders
- Delivered Orders
- Cancelled Orders
- Cancellation Rate
- Delivery Rate
- Order Status Distribution
- Orders by Payment Method
- Revenue by Payment Method
- Orders Trend
- Cancellation by Payment Method
- Cancellation Rate by City
- Order Status Over Time

### 5. Customer Value & Retention
- Repeat Customer Rate
- Revenue per Customer
- Average Orders per Customer
- Repeat Customers
- Revenue by Customer Type
- Customers by Customer Type
- Top High-Value Customers
- City Repeat Customer Rate
- Customer Tenure vs Revenue
- Purchasing Frequency by Customer Type
- Revenue Contribution by Segment

### 6. Executive Summary
The executive dashboard brings together:
- Total Revenue
- Total Orders
- Total Customers
- Average Order Value
- Repeat Customer Rate
- Cancellation Rate
- Total Quantity Sold
- Top Category
- Revenue Trend
- Revenue by Category
- Revenue by Customer Segment
- Orders by Payment Method
- Top Products
- Key Business Insights
- Business Recommendations

## Business Insights
The analysis is designed to identify:
- Revenue contribution from different categories and products
- Sales trends over time
- City-level sales performance
- Customer purchasing and repeat behaviour
- High-value customer segments
- Product demand and stock-related patterns
- Delivery and cancellation patterns
- Payment method usage and revenue contribution
- Customer value and retention patterns

## Business Recommendations
1. Focus marketing efforts on high-performing categories and products.
2. Prioritize inventory for products with strong demand.
3. Monitor low-stock products to reduce stock-out risk.
4. Use targeted promotions for products with high stock and lower sales.
5. Develop loyalty and personalized offers for repeat and high-value customers.
6. Investigate cities with higher cancellation rates.
7. Monitor payment methods based on order volume, revenue, and cancellation patterns.
8. Use city-level performance to support localized marketing strategies.
9. Use monthly sales trends for inventory and promotional planning.
10. Review consistently low-performing products before future procurement.

## Tools & Technologies
- **Microsoft Power BI**
- **Power Query**
- **DAX**
- **Microsoft Excel**

## Project Structure
```text
E-Commerce-Sales-Customer-Product-Analytics/
│
├── E-Commerce_Sales_Customer_Product_Analytics.pbix
├── README.md
│
└── screenshots/
    ├── data-cleaning.png
    ├── model-view.png
    ├── sales-performance.png
    ├── customer-analytics.png
    ├── product-category.png
    ├── orders-payment.png
    ├── customer-retention.png
    └── executive-summary.png
```

## Deliverables
- Power BI `.pbix` project file
- Data cleaning evidence
- Data model
- Interactive Power BI dashboards
- Business insights
- Business recommendations
