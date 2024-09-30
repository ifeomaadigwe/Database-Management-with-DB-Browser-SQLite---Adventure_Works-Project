# Database-Management-with-DB-Browser-SQLite---Adventure_Works-Project

Creating a Database using DB Browser for SQLite

The Adventure_work project demonstrates how to design, build, and query a relational database using DB Browser for SQLite. The design includes schema creation, data manipulation, Entity Relationship Diagram (ERD) and SQL query for effective database management using DB Browser for SQLite. 
The database models key aspects of a fictional retail business, tracking customers, products, sales, returns, and territories. 
This repository includes SQL scripts for schema creation and manipulation, making it a practical reference for database management and query operations.

Database Schema Overview
The database is structured around several interconnected tables to handle various business processes such as customer management, product categorization, sales, and returns. Below is a summary of the main tables included in the schema:

1. AdventureWorks_Customers
This table stores customer details, including demographic information and personal data such as:
CustomerKey (Primary Key)
First Name, Last Name, Birth Date
Marital Status, Gender, Occupation
Annual Income, Total Children
Contact information like Email Address

2. AdventureWorks_Calendar
A simple calendar table used to track dates across the database. It includes:
Date (Primary Key)

3. AdventureWorks_Product_Categories
This table defines the major product categories in the inventory, including:
ProductCategoryKey (Primary Key)
CategoryName

4. AdventureWorks_Product_Subcategories
Each product category can have multiple subcategories. This table includes:
ProductSubcategoryKey (Primary Key)
SubcategoryName
ProductCategoryKey (Foreign Key referencing Product Categories)

5. AdventureWorks_Products
The core table for product data, which includes:
ProductKey (Primary Key)
ProductSubcategoryKey (Foreign Key referencing Product Subcategories)
Details like Product Name, SKU, Model Name, Price, Cost, and more.

6. AdventureWorks_Territories
This table defines sales territories with geographic details:
SalesTerritoryKey (Primary Key)
Region, Country, Continent

7. AdventureWorks_Returns
Records returns of products, including:
ReturnDate (Foreign Key referencing Calendar)
TerritoryKey, ProductKey (Foreign Keys referencing Territories and Products)
ReturnQuantity

8. AdventureWorks_Sales_2015, 2016, 2017
Sales data for three consecutive years, each stored in separate tables with:
OrderDate, StockDate (Foreign Keys referencing Calendar)
OrderNumber (Primary Key)
ProductKey, CustomerKey, TerritoryKey (Foreign Keys referencing relevant tables)
OrderLineItem, OrderQuantity


Key Features
Relational Design: 
The database is designed with strong relational integrity, utilizing foreign key constraints to enforce data consistency across customers, products, sales, and returns.
Normalization: Product categories and subcategories are normalized to reduce redundancy and ensure better data organization.
Temporal Data: The calendar table enables tracking of dates for orders and returns, supporting time-based analysis.
Multi-year Sales Data: Sales data is broken down by year, allowing for longitudinal analysis of business performance.
