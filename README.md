
# Amazon Sales Dashboard

### Dashboard Link :https://app.powerbi.com/groups/me/reports/3b0befda-be6e-400a-9d50-05ada64dbc25/1caf0161526cc8135e40?experience=power-bi&clientSideAuth=0

## Problem Statement

This dashboard provides a detailed analysis of Amazon's sales performance across various regions, customer segments, and product categories. It helps Amazon identify top-performing products, regions, and customers while also highlighting key areas of improvement, such as products with significant losses and underperforming regions. The dashboard enables decision-makers to take data-driven actions for improving sales and profitability.


### Steps followed 

Step 1: Data was imported into Power BI from an Excel file.

Step 2: Opened Power Query Editor and selected the "Column Distribution", "Column Quality", and "Column Profile" options from the View tab for data profiling.

Step 3: Applied full column profiling across the entire dataset to get a comprehensive view of the data quality.

Step 4: Cleaned the data by removing any null values and errors. Ensured data integrity across key fields such as "Product Name", "Region", "Customer Name", and "Sales".

Step 5: In the report view, a theme was selected for better visual appeal.

Step 6: Slicers were added for filtering the data by year (2012-2015) and region (e.g., Europe, North America, Asia Pacific).

Step 7: Card visuals were added to display key performance indicators (KPIs) such as total units sold, projected sales, and return counts.

Step 8: A pie chart was created to visualize sales by customer segment (Home Office, Consumer, Corporate).

Step 9: A regional map was used to display sales distribution across different geographic regions like North America, Europe, Asia Pacific, and Latin America.

Step 10: Bar charts were created to show profits by top customers and losses by underperforming products.

Step 11: A calculated column was created to categorize customers by region using the following DAX expression:

        Region Group = IF(amazon_sales_data[Region]="US", "United States", 
                  IF(amazon_sales_data[Region]="EU", "Europe", "Other Regions"))

Step 12: New measures were created to calculate total sales, profits, and losses. The following DAX expression was used to calculate total sales:

        Total Sales = SUM(amazon_sales_data[Sales])
        % Sales by Region = DIVIDE(SUM(amazon_sales_data[Sales]), [Total Sales])*100

Step 13: Visual filters (slicers) were added for product categories and regions to allow for dynamic analysis.

Step 14: Text boxes were added to display Amazon’s tagline and other key information.

Step 15: Finally, the report was published to Power BI Service for real-time sharing and collaboration.




# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](![Screenshot 2024-10-15 190319](https://github.com/user-attachments/assets/ee194838-9c7d-4317-ae8c-7019e0defca1)


 


# Insights

Total Sales: $12.64M

Total Units Sold: 3,788 units

Total Returns: 1,464 products returned

Projected Sales: $178K

### [1] Sales by Segment

Home Office Segment: 6.51M (51.48%)

Corporate Segment: 3.82M (30.25%)

Consumer Segment: 2.31M (18.27%)
           
### [2] Sales by Region

USCA (United States & Canada): 4.04M (31.98%)

Africa: 3.29M (26%)

LATAM (Latin America): 2.36M (18.7%)

Europe: 2.16M (17.12%)

Asia Pacific: 0.78M (6.2%)

        The United States & Canada lead Amazon’s sales, followed by Africa and Latin America.
  

  
  ### [3] Top 5 Profitable Products

  
Canon ImageCLASS Printer: $25K profit

Cisco Smart Phone: $17K profit

Motorola Smart Phone: $17K profit

        These are the top products generating the highest profits.

 ### [4] Top 5 Loss-Making Products
Cubify Cube 3: -$8.9K loss

Lexmark MX611: -$4.6K loss

Motorola Smart Phone: -$4.4K loss

        These products are contributing to the highest losses, indicating a need for investigation and action.
         
### Sales by Customer Type
Returning Customers: 81.69%

First-Time Customers: 18.31%

        A majority of sales come from returning customers, highlighting strong customer loyalty.


### Sales by Travel Type
Business Travel: 69.06%

Personal Travel: 30.94%

        Business-related purchases dominate the sales data.
# Publishing
The report was successfully published to Power BI Service, making it accessible for real-time updates and insights.
