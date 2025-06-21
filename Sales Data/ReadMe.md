# Sales Data EDA

An exploratory data analysis (EDA) project focused on understanding sales patterns across customers, regions, and order statuses. 
The analysis leverages descriptive statistics and visualizations to generate insights into pricing, product lines, and sales behavior.
In this project, dynamic arrays were mostly used to answer the questions, without relying on traditional pivot tables, except for the use of the PIVOTBY() function in one instance, as indicated below.

------------------------

## Project Structure

- The whole project is located in workbook `Sales_Data_Project.xlsx`, which contains the following four worksheets:

    - `Table of Contents`: A simple TOC that links to the location of the dataset, each question and the small dashboard included.
    - `Data`: The sales dataset used for the analysis.
    - `S1. Answers`: Contains the answers to the questions for the analysis.
    - `S2. Small Dashboard`: Contains a small dashboard providing a quick summary of the product lines by each order status

- In `Detailed Results` the detailed insights from the data are located.

TODO: TOC for results

## Tools Used

`Microsoft Excel 365`


## Methods

TODO



## Questions

**I. Univariate Analysis**

1. **Missing values** and **frequencies** for some of the categorical variables.
    
2. Discriptive statistics for some of the numerical variables at the **order item-level** (row-level).
    
3. Discriptive statistics for some of the numerical variables at the **order-level**.
    
4. **Extreme outliers** in item sales.
    
**II. Multivariate Analysis**

**A. Seasonality**
  
1. Quick summary of **total item sales** over the years by each **quarter**.
    
2. Average **monthly discount rate** for each **product line**.
    
**B. Sales and Revenue**
  
1. Top 5 **countries** and **regions** that generate the **most revenue** from purchases.
    
2. **Average order value** by **country**.
    
3. Top 10 **countries** by **order volume**.
    
**C. Customer Behaviour**
  
1. Top and bottom 5 **customers** by **orders** placed.
    
2. Top and bottom 5 customers by **average individual** order item **sales**.
    
3. **Countries** sorted from the highest to least amount of **return customers**.
    
4. Most popular **product lines** by **region** and **country**.
    
**D. Product-Level Analysis**
  
1. Top and bottom 10 **most ordered products**.
    
2. Top and bottom 5 **products** by **order volume**. 
    
3. Top **product lines** based on **total sales**.
    
4. **Average discount rate** per **country** and **region**.
    



## Insights

### Data Overview

- Order items for each order are listed in different rows, resulting to more than one rows for each order.
- All observations in the dataset include relevant data, with most missing values occuring for the second adress line, state or postal code.
  
### Sales & Pricing Analysis
- On average approximately 34.93 ± 9.36 units are ordered by product, but 320.91 ± 174.88 units by order.
- On average approximately the price of a product ordered is 83.64 ± 20.24, but the total price of an order is approximately 768.37 ± 418.08.
- On average approximately the sale of a product ordered is 3544.38 ± 1819.72, but the total sales of an order are approximately 32559.38 ± 17691.56.
- On average approximately the MSRP of a product ordered is 100.89 ± 40.44, but the total price of an order is approximately 926.84 ± 509.24.
- Since on average MSRP > price of each product, then that means that the business on average sells bellow the full price.
- On average, outliers exist for item sales in the upper end of sales and quantity ordered.

### Customer Behavior
- Most frequently ordered products belong to the Classic Cars, Vintage Cars, and Motorcycles product lines.
- Euro Shopping Channel has placed the most orders, with most ordered items being Classic Cars, while least ordered items being Trains.
- Bavarian Collectables Imports, Co. is the only one-time customer.
- Among return customers Super Scale Inc. orders on average the most expensive individual order items, while Australian Collectables, Ltd orders on average the least expensive individual order items.
- Even though Euro Shopping Channel has placed the most orders, the customer has not placed in the top 5 customers.
- Classic Cars are by far the most ordered product lines.

### Geographic Patterns
- When beaking down the orders's count by region the majority of orders are placed from Europe followed closely by North America. However, breaking down the orders's count by country, the majority are placed from USA.
- Breaking down revenue by country, USA by far generates the most revenue, while breaking down revenue by region, Europe generates the most revenue.
This is caused by the fact that even though the most orders and order volume are placed from the USA, its average order value ranks around the middle compared to the other countries.
- Switzerland and Ireland are among the countries with the least orders placed.
Howeever, even though Switzerland is among the two countries with the least orders and also in the bottom 4 for volume ordered, on average the most expensive orders are placed from there, while Ireland has the least volume ordered among all countries.
- USA has by far the most return customers, considering the fact that by far the most placed orders are done from there.
- France ranks second in both total orders and return customers, showing a consistent pattern between order activity and customer loyalty.


### Temporal Trends
- Overall best quarter was Q4 in 2004 and worst Q1 in 2003.
- The most overcharges are happening in December for Trains.
- The biggest discount happens in June for Classic Cars.

  
### Product Line Insights
- Vintage Cars are most ordered by Australia, Belgium and Italy,  Trucks and Buses are most ordered by Canada,  Planes are most ordered by Japan, while for the rest of countries Classic Cars.

### Order Status & Performance


### Operational Insights
- On average, Trains are overcharged, but Classic Cars,  Motorcycles, Trucks and Buses are discounted.


## License
> The dataset used in this project is licensed under the [CC BY-NC-SA 3.0 license](https://creativecommons.org/licenses/by-nc-sa/3.0/) and is available at [Kaggle](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data/data).

## TODO



