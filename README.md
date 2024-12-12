# Property Management Dashboard

 ![Property Management Dashboard](https://github.com/Azmary413/Property-Management-Dashboard-using-Power-BI/blob/main/Output/Dashboard.jpg)

## Overview
This project involves a dynamic and interactive Power BI dashboard designed for managing and analyzing property-related data. The dashboard provides insights into revenue, expenses, income, sales performance, property details, and client information, offering a comprehensive view of property management operations.

## Features
- **Key Metrics:** Displays revenue, expenses, income, and properties sold.
- **Revenue Analysis:** Revenue segmented by month, sales type, property type, and country.
- **Sales Summary:** Detailed information on property sales, including location, sale date, price, and payment status.
- **Client Insights:** Highlights top clients with revenue contribution and occupation.
- **Property Details:** Displays the most expensive property with key attributes such as bedroom count, bathroom count, square footage, and price.
- **Custom Visualizations:** Includes:
  - Custom calendar for date-based filtering.
  - SVG-based column for visual representation of payment status.
  - Interactive map visualization for revenue by country.
  - Comprehensive table modeling for relational data representation.

## Advanced Techniques
- **Custom Calendar:** Used to create date hierarchies and precise time-based filtering, ensuring better time intelligence functionalities.
- **SVG Integration:** Implemented SVG columns to visually represent payment statuses dynamically.
- **Data Modeling:** Designed a robust data model connecting five relational tables for seamless data integration and analysis. The model ensures normalized data and efficient querying.
- **Interactive Filters:** Enabled advanced filtering options for in-depth exploration of data.

## Dataset
The dataset consists of five tables:

1. **Client Table:**
   - `ClientID`: Unique identifier for each client.
   - `Name`: Client's name.
   - `Occupation`: Client's occupation.
   - `Img`: Profile image of the client.

2. **Expense Table:**
   - `ExpenseID`: Unique identifier for each expense.
   - `PropertyID`: Identifier linking to the property table.
   - `ExpenseType`: Type of expense.
   - `Amount`: Expense amount.
   - `Date`: Expense date.

3. **Property Table:**
   - `PropertyID`: Unique identifier for each property.
   - `Country`: Country where the property is located.
   - `Type`: Property type (Apartment, Condo, Single Family, Townhouse).
   - `Bedrooms`: Number of bedrooms.
   - `Bathrooms`: Number of bathrooms.
   - `SquareFootage`: Property size in square feet.
   - `Price`: Property price.
   - `ListedDate`: Date the property was listed.
   - `Status`: Property status (e.g., sold, available).
   - `Img`: Property image.
   - `Location`: Property address.

4. **Sales Table:**
   - `SaleID`: Unique identifier for each sale.
   - `PropertyID`: Identifier linking to the property table.
   - `SaleDate`: Date of sale.
   - `Means of Sales`: Sales channel (e.g., online, broker, direct).
   - `ClientID`: Identifier linking to the client table.
   - `Payment Status`: Payment status (Paid, Pending).

5. **Custom Calendar:**
   - Used to create date hierarchies and ensure precise time-based filtering.

## Table Modeling

![Table Modeling Diagram](https://github.com/Azmary413/Property-Management-Dashboard-using-Power-BI/blob/main/Output/Model%20View.jpg)

The dashboard employs a well-structured relational data model connecting all tables:
- **Relationships:**
  - `Property_Table` is connected to `Sales_Table` and `Expense_Table` via `PropertyID`.
  - `Sales_Table` links to `Client_Table` via `ClientID`.
  - A custom `Calendar` table is connected to `Sales_Table` and `Expense_Table` via the `Date` column.
- **Measures:**
  - Created custom measures for calculating revenue, income, and expense trends.
  - Utilized DAX for advanced calculations, including year-over-year growth, revenue distribution, and dynamic colors.


## Key Insights
1. **Revenue Trends:**
   - The highest monthly revenue was observed in July, reaching 6.1M.
   - Revenue distribution by sales type indicates that online sales contribute the most (9.5M).

2. **Property Insights:**
   - Apartments account for 27.06% of the total revenue.
   - The most expensive property is an apartment with 1 bedroom, 1 bathroom, and 1800 sq. ft., priced at 1M.

3. **Geographic Distribution:**
   - India leads in revenue generation with 5.1M, followed by Mexico and Brazil.

4. **Client Contribution:**
   - Top client Emily Davis, a lawyer, contributed 5.2M in revenue.

## How to Use
1. Download the `.pbix` file from the repository.
2. Open the file in Power BI Desktop.
3. Explore the dashboard for insights on property management.

