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

- In `Detailed Results` the questions and the detailed insights infered from the data are located.


- [I. Indroduction to the Dataset](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#i-indroduction-to-the-dataset)

- [II. Univariate Analysis](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#i%CE%B9-univariate-analysis)

    - [1. **Missing values** and **frequencies** for some of the categorical variables.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#1-missing-values-and-frequencies-for-some-of-the-categorical-variables)
    
    - [2. Discriptive statistics for some of the numerical variables at the **order item-level** (row-level).](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#2-discriptive-statistics-for-some-of-the-numerical-variables-at-the-order-item-level-row-level)
    
    - [3. Discriptive statistics for some of the numerical variables at the **order-level**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#3-discriptive-statistics-for-some-of-the-numerical-variables-at-the-order-level)
    
    - [4. **Extreme outliers** in item sales.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#4-extreme-outliers-in-item-sales)
    
- [**III. Multivariate Analysis**](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#ii%CE%B9-multivariate-analysis)

    - [**A. Seasonality**](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#a-seasonality)
  
        - [1. Quick summary of **total item sales** over the years by each **quarter**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#1-quick-summary-of-total-item-sales-over-the-years-by-each-quarter)
    
[2. Average **monthly discount rate** for each **product line**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#2-average-monthly-discount-rate-for-each-product-line)
    
[**B. Sales and Revenue**](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#b-sales-and-revenue)
  
[1. Top 5 **countries** and **regions** that generate the **most revenue** from purchases.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#1-top-5-countries-and-regions-that-generate-the-most-revenue-from-purchases)
    
[2. **Average order value** by **country**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#2-average-order-value-by-country)
    
[3. Top 10 **countries** by **order volume**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#3-top-10-countries-by-order-volume)
    
[**C. Customer Behaviour**](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#c-customer-behaviour)
  
[1. Top and bottom 5 **customers** by **orders** placed.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#1-top-and-bottom-5-customers-by-orders-placed)
    
[2. Top and bottom 5 customers by **average individual** order item **sales**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#2-top-and-bottom-5-customers-by-average-individual-order-item-sales)
    
[3. **Countries** sorted from the highest to least amount of **return customers**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#3-countries-sorted-from-the-highest-to-least-amount-of-return-customers)
    
[4. Most popular **product lines** by **region** and **country**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#4-most-popular-product-lines-by-region-and-country)
    
[**D. Product-Level Analysis**](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#d-product-level-analysis)
  
[1. Top and bottom 10 **most ordered products**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#1-top-and-bottom-10-most-ordered-products)
    
[2. Top and bottom 5 **products** by **order volume**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#2-top-and-bottom-5-products-by-order-volume)
    
[3. Top **product lines** based on **total sales**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#3-top-product-lines-based-on-total-sales)
    
[4. **Average discount rate** per **country** and **region**.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#4-average-discount-rate-per-country-and-region)


## Tools Used

`Microsoft Excel 365`


## Methods

TODO

   


## Insights

### Data Overview

- Order items for each order are listed in different rows, resulting to more than one rows for each order.
- All observations in the dataset include relevant data, with most missing values occuring for the second adress line, state or postal code.

### Order Status
- The vast majority of orders are shipped (93.16%), with a minority of them in process, cancelled, on hold, resolved or disputed.
- Removal of Cancelled, On Hold and Disputed orders was done, in order to analize the sales variables.

    
### Sales & Pricing Analysis
- On average approximately 34.93 ± 9.36 units are ordered by product, but 320.91 ± 174.88 units by order.
- On average approximately the price of a product ordered is 83.64 ± 20.24, but the total price of an order is approximately 768.37 ± 418.08.
- On average approximately the sale of a product ordered is 3544.38 ± 1819.72, but the total sales of an order are approximately 32559.38 ± 17691.56.
- On average approximately the MSRP of a product ordered is 100.89 ± 40.44, but the total price of an order is approximately 926.84 ± 509.24.
- Since on average MSRP > price of each product, then that means that the business on average sells bellow the full price.
- On average, outliers exist for item sales in the upper end of sales and quantity ordered.
- On average, Trains are overcharged, but Classic Cars,  Motorcycles, Trucks and Buses are discounted.
  
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
- On average, the most discounted orders by country, are for Switzerland (18.61%), while the least discounted orders are for Spain (6.68%).
However, on average, the most discounted orders by territory are for Japan (12.75%), while the least discounted orders are for APAC (8.60%).

### Temporal Trends
- Overall best quarter was Q4 in 2004 and worst Q1 in 2003.
- The most overcharges are happening in December for Trains.
- The biggest discount happens in June for Classic Cars.

  
### Product Line Insights
- Classic cars are by far the most sold products, followed by Vintage Cars, while Trains are by far the least sold products.
- Vintage Cars are most ordered by Australia, Belgium and Italy,  Trucks and Buses are most ordered by Canada,  Planes are most ordered by Japan, while for the rest of countries Classic Cars.
- The most ordered product is S18_3232, that belong to the Classic Cars line, while the least ordered products are S18_1749, S18_2248, S18_4409, S18_4933, S24_2887, S24_3969 that belong to the Vintage and Classic Cars lines.
- Most products that are in the top 10 most ordered volume are part of the Trucks and Buses line, while for the bottom 10 they are part of either the Classis or Vintage Cars line.



## License
> The dataset used in this project is licensed under the [CC BY-NC-SA 3.0 license](https://creativecommons.org/licenses/by-nc-sa/3.0/) and is available at [Kaggle](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data/data).

## TODO



