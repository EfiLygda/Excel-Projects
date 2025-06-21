# Datailed Results

## Table of Contents

- [I. Indroduction to the Dataset](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#i-indroduction-to-the-dataset)


- [II. Univariate Analysis](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#i%CE%B9-univariate-analysis)

    - [1. Missing values and frequencies.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#1-missing-values-and-frequencies-for-some-of-the-categorical-variables)
    
    - [2. Discriptive statistics at the order item-level (row-level).](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#2-discriptive-statistics-for-some-of-the-numerical-variables-at-the-order-item-level-row-level)
    
    - [3. Discriptive statistics at the order-level.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#3-discriptive-statistics-for-some-of-the-numerical-variables-at-the-order-level)
    
    - [4. Extreme outliers in item sales.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#4-extreme-outliers-in-item-sales)
    
- [III. Multivariate Analysis](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#ii%CE%B9-multivariate-analysis)

    - [A. Seasonality](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#a-seasonality)
  
        - [1. Total item sales over the years by each quarter.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#1-quick-summary-of-total-item-sales-over-the-years-by-each-quarter)
    
        - [2. Average monthly discount rate by product line.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#2-average-monthly-discount-rate-for-each-product-line)
    
    - [B. Sales and Revenue](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#b-sales-and-revenue)
  
        - [1. Top 5 countries and regions by revenue.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#1-top-5-countries-and-regions-that-generate-the-most-revenue-from-purchases)
    
        - [2. Average order value by country.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#2-average-order-value-by-country)
    
        - [3. Top 10 countries by order volume.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#3-top-10-countries-by-order-volume)
    
    - [C. Customer Behaviour](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#c-customer-behaviour)
  
        - [1. Top and bottom 5 customers by orders placed.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#1-top-and-bottom-5-customers-by-orders-placed)
    
        - [2. Top and bottom 5 customers by average individual order item sales.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#2-top-and-bottom-5-customers-by-average-individual-order-item-sales)
    
        - [3. Sorted Countries by return customers.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#3-countries-sorted-from-the-highest-to-least-amount-of-return-customers)
    
        - [4. Most popular product lines by region and country.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#4-most-popular-product-lines-by-region-and-country)
    
    - [D. Product-Level Analysis](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#d-product-level-analysis)
  
        - [1. Top and bottom 10 most ordered products.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#1-top-and-bottom-10-most-ordered-products)
    
        - [2. Top and bottom 5 products by order volume.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#2-top-and-bottom-5-products-by-order-volume)
    
        - [3. Top product lines by total sales.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#3-top-product-lines-based-on-total-sales)
    
        - [4. Average discount rate per country and region.](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#4-average-discount-rate-per-country-and-region)



-------------------

## I. Indroduction to the Dataset

The number of rows of the dataset is 2823, while the number of columns is 25. 
Bellow the column names and a brief descriction of each column is presented:

| Column Name        | Description                                                |
| ------------------ | ---------------------------------------------------------- |
| `ORDERNUMBER`      | Unique identifier for each order                           |
| `QUANTITYORDERED`  | Number of units ordered in the line item                   |
| `PRICEEACH`        | Unit price for the product in the order                    |
| `ORDERLINENUMBER`  | Line item number in the order                              |
| `SALES`            | Total sales amount                                         |
| `ORDERDATE`        | Date when the order was placed                             |
| `STATUS`           | Current order status (`Shipped`, `Cancelled` etc.)         |
| `QTR_ID`           | Quarter number of the year (1, 2, 3, 4)                    |
| `MONTH_ID`         | Month number (1–12)                                        |
| `YEAR_ID`          | Year (2003, 2004, 2005)                                    |
| `PRODUCTLINE`      | Product category or line (`Classic Cars`, `Motorcycles` etc.)  |
| `MSRP`             | Manufacturer's Suggested Retail Price                      |
| `PRODUCTCODE`      | Unique product identifier                                  |
| `CUSTOMERNAME`     | Name of the customer                                       |
| `PHONE`            | Customer’s phone number                                    |
| `ADDRESSLINE1`     | Primary address line                                       |
| `ADDRESSLINE2`     | Secondary address line (if any)                            |
| `CITY`             | City of the customer                                       |
| `STATE`            | State or province (if available)                           |
| `POSTALCODE`       | Customer’s postal or ZIP code                              |
| `COUNTRY`          | Country of the customer                                    |
| `TERRITORY`        | Sales territory or region                                  |
| `CONTACTLASTNAME`  | Contact person’s last name                                 |
| `CONTACTFIRSTNAME` | Contact person’s first name                                |
| `DEALSIZE`         | Deal size classification (Small, Medium, Large)            |


> [!NOTE]
> - By grouping the data by `ORDERNUMBER`, it is noted that `total orders` < `number of rows`.
>  This fact, along with the fact that no dublicate rows were found, indicates that each product purchased in an order, is listed in a different row than the other ones, with the `ORDERLINENUMBER` column indicating the way that the products were placed in the order.
> - There are discrepancies when calculating `SALES` as `QUANTITYORDERED * PRICEEACH`, since prices > 100 in `PRICEEACH` column are capped at 100, as per the [this discussion](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data/discussion/82824#1188157) on the dataset.


## IΙ. Univariate Analysis

#### 1. Missing values and frequencies.

- All observations in the dataset include relevant data, with most missing values occuring for the second adress line, state and then postal code.

- The vast majority of orders are shipped (93.16%), with a minority of them in process, cancelled, on hold, resolved or disputed.

- The most frequently ordered products belong to the Classic Cars, Vintage Cars, and Motorcycles product lines. More data would be needed to inferr if these products are for personal use.

- When beaking down the orders's count by region the majority of orders are placed from Europe followed closely by North America. However, breaking down the orders's count by country, the majority are placed from USA.

- Most orders do not list a state, but for USA based clients most orders were placed from California.

- Madrid, Spain is the most frequent city by order count, with 31 orders recorded. This aligns with the broader trend of significant European participation in orders.

    
#### 2. Discriptive statistics at the order item-level (row-level).

- Removal of Cancelled, On Hold and Disputed orders was done, in order to analize the variables.

- The average quantity ordered (QUANTITYORDERED) for each item in an order is approximately 34.93 ± 9.36 units.
The distribution appears to be approximately symmetric (skewness ≈ 0.24), but with a slight platykurtic shape (kurtosis ≈ -0.08), indicating a flatter shape with light tails, thus suggesting slightly less prone towards outliers distribution, compared to the normal distribution.

- The average unit price (PRICEEACH) for each item in an order is approximately 83.64 ± 20.24 currency.
The distribution appears to be moderately to highly left-skewed (skewness ≈ -0.94), due to the fact that, as per the dataset's author's comments, prices over 100 are capped at 100 currency causing most of the prices to crowd at the upper end of the distribution.
It also appears to have a slightly platykurtic shape (kurtosis ≈ -0.39), indicating a flatter shape with lighter tails, thus suggesting it is slightly less prone to outliers, compared to the normal distribution.

- The average sales (SALES) for each item in an order is approximately 3544.38 ± 1819.72 currency.
The distribution appears to be highly right-skewed (skewness ≈ 1.12), indicating a tendency for a few higher priced sales to pull the mean upwards.
It also appears to have a highly leptokurtic shape (kurtosis ≈ 1.50), suggesting it is peaked and more prone to outliers, compared to the normal distribution.

- The average Manufacturer's Suggested Retail Price (MSRP) for each item in an order is approximately 100.89 ± 40.44 currency.
The distribution appears to be moderately right-skewed (skewness ≈ 0.58), indicating a tendency for a few higher priced units to pull the mean upwards
It also appears to have a slightly platykurtic shape (kurtosis ≈ -0.15, suggesting it is flatter and lightly less prone to outliers, compared to the normal distribution.

- Since on average MSRP > PRICEEACH, then that means that the business on average sells bellow the full price of each product.


    
#### 3. Discriptive statistics at the order-level.

- Removal of Cancelled, On Hold and Disputed orders was done, in order to analysize the variables.

- The average quantity ordered (QUANTITYORDERED) for each order is approximately 320.91 ± 174.88 units.
The distribution appears to be approximately symmetric (skewness ≈ 0.08), but with a highly platykurtic shape (kurtosis ≈ -1.02) indicating a flatter shape with lighter tails, thus suggesting it is less prone to outliers, compared to the normal distribution.

- The average total unit price (PRICEEACH) in each order is approximately 768.37 ± 418.08 currency.
The distribution appears to be approximately symmetric (skewness ≈ 0.00), but with a highly platykurtic shape (kurtosis ≈ -1.14) indicating a flatter shape with lighter tails, thus suggesting it is less prone to outliers, compared to the normal distribution.

- The average sales (SALES) for each order is approximately 32559.38 ± 17691.56 currency.
The distribution appears to be approximately symmetric (skewness ≈ 0.03), but with a moderately to highly platykurtic shape (kurtosis ≈ -0.93) indicating a flatter shape with lighter tails, thus suggesting it is less prone to outliers, compared to the normal distribution.

- The average Manufacturer's Suggested Retail Price (MSRP) for each order is approximately 926.84 ± 509.24 products.
The distribution appears to be approximately symmetric (skewness ≈ 0.01), but with a platykurtic shape (kurtosis ≈ -1.06) indicating a flatter shape with lighter tails, thus suggesting it is less prone to outliers, compared to the normal distribution.

- Since on average MSRP > PRICEEACH, then that means that the business on average sells bellow the full price of each order.

- Comparing the analysis done at the item-level with the analysis done at order-level, the distributions at the order level appear more robust  by being generally more symmetric and significantly less prone to outliers.


    
#### 4. Extreme outliers in item sales.

- Using Z-score to identify outliers, 30 item sales were found. All of them were in the upper end of sales.
- Using Interquartile Range to identify outliers, 81 item sales were found. All of them were in the upper end of sales.
- On average, using both methods, outliers are in the upper end of sales and quantity. 

    
## IIΙ. Multivariate Analysis

### A. Seasonality
  
#### 1. Total item sales over the years by each quarter.

- Removal of Cancelled, On Hold and Disputed orders was done, in order to analysize the variables.
- Data for Q3 and Q4 in 2005 is not available. Insights for 2005 will be limited.
- Sales in 2004 were higher than 2003, on average.
- Best sales performance was in Q4 for both 2003 and 2004, but in Q1 for 2005.
- Worst sales performance in Q1 for 2003, Q2 for 2004 and 2005.
- Overall best quarter was Q4 in 2004 and worst Q1 in 2003.

    
#### 2. Average monthly discount rate for each product line.

- Negative discounts mean that products are on average sold above the MSRP, meaning that they are overcharged.
- On average, Trains are overcharged, but Classic Cars are discounted.
- Motorcycles, Trucks and Buses are, on average, discounted.
- The most overcharges are happening in December for Trains, sold on average 32% more than the orginal price.
- The biggest discount happens in June for Classic Cars, with a 23% discount.


### B. Sales and Revenue
  
#### 1. Top 5 countries and regions by revenue.

- Breaking down revenue by country, USA by far generates the most revenue.
- Breaking down revenue by region, Europe generates the most revenue, followed by North America.
- Since only 4 regions' data are available Japan generates the least revenue.

    
#### 2. Average order value by country.

- Even though Switzerland is among the two countries with the least orders (2 to be exact), on average the most expensive orders are placed from there.
- While Belgium has a total 7 orders placed they are the least expensive, on average.
- Even though by far the most orders are placed from the USA, the average order value ranks around the middle compared to the other countries.

    
#### 3. Top 10 countries by order volume.

- The most volume is ordered by USA, complying with the fact that most orders are placed from there.
- The least volume is ordered by Ireland, complying with the fact that Ireland, along with Switzerland, are among the two countries with least amount of orders placed.
- Switzerland is among the bottom 4 countries with the least total order volume.
However, considering that the average order value from Switzerland is the highest, this suggests that the items ordered tend to be more expensive. Still, this assumption warrants further investigation.


### C. Customer Behaviour
  
#### 1. Top and bottom 5 customers by orders placed.

- Euro Shopping Channel has placed the most orders with most ordered items being Classic Cars, while least ordered items being Trains.
- Bavarian Collectables Imports, Co. is the only one-time customer. In the order the most ordered items were Planes, while the least ordered items were Ships.
- Except from Bavarian Collectables Imports, Co. every other customer is a return-customer.

    
#### 2. Top and bottom 5 customers by average individual order item sales.

- Super Scale Inc. orders on average the most expensive individual order items, while Bavarian Collectables Imports, Co. orders on average the least expensive individual order items.
- Classic Cars seem to be the most ordered items for the top 5 customers by average item sales, while Planes, Vintage Cars and Classic Cars seem to be the most ordered by the bottom 5 customers.
- Ships, Vintage Cars, Planes and Trains seem to be the least ordered items for the top 5 customers by average item sales, while Ships, Classic Cars and Vintage Cars seem to be the least ordered by the bottom 5 customers.
 Bavarian Collectables Imports, Co. is the only one-time customer and also the one with least average order item value.
- Even though Euro Shopping Channel has placed the most orders, the customer has not placed in the top 5 customers.


    
#### 3. Sorted countries by return customers.

- USA has by far the most return customers, considering the fact that by far the most placed orders are done from there.
- France ranks second in both total orders and return customers, showing a consistent pattern between order activity and customer loyalty.
- All other countries with return customers have fewer than 10 return customers each, highlighting a steep drop-off beyond the top two countries.



#### 4. Most popular product lines by region and country.

- Classic Cars are by far the most ordered product lines in the whole dataset, but also for most countries.
- Vintage Cars are most ordered by Australia, Belgium and Italy.
- Trucks and Buses are most ordered by Canada.
- Planes are most ordered by Japan.
- Motorcycles and Ships did not show up as most ordered by none of the countries.




### D. Product-Level Analysis
  
#### 1. Top and bottom 10 most ordered products.

- The most ordered product is S18_3232, that belong to the Classic Cars line.
- The least ordered products with same frequencies are S18_1749, S18_2248, S18_4409, S18_4933, S24_2887, S24_3969 that belong to the Vintage and Classic Cars lines.
- The top 10 products are either in the Classic Cars or Trucks and Buses line.

    
#### 2. Top and bottom 5 products by order volume.

- The product with the most ordered volume is S18_3232, that is also the most ordered product.
- The product with the least ordered volume is S18_4933, the is part of the Classic Cars line.
- Most products that are in the top 10 most ordered volume are part of the Trucks and Buses line, while for the bottom 10 they are part of either the Classis or Vintage Cars line.

    
#### 3. Top product lines based on total sales.

- Classic cars are by far the most sold products, followed by Vintage Cars.
- Trains are by far the least sold products.

    
#### 4. Average discount rate per country and region.

- On average most orders are discounted, a fact encountered in Q.II.3. 
- On average, by country the most discounted orders are for Switzerland (18.61%), while the least discounted orders are for Spain (6.68%).
- On average, by territory the most discounted orders are for Japan (12.75%), while the least discounted orders are for APAC (8.60%).



