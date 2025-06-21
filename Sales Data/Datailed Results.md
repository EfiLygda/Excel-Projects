# Datailed Results

Bellow the insights from the questions are presented in detail.

-------------------

**I. Indroduction to the Dataset**

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
| `STATUS`           | Current order status (Shipped, Cancelled etc.)             |
| `QTR_ID`           | Quarter number of the year (1, 2, 3, 4)                    |
| `MONTH_ID`         | Month number (1–12)                                        |
| `YEAR_ID`          | Year (2003, 2004, 2005)                                    |
| `PRODUCTLINE`      | Product category or line (Classic Cars, Motorcycles etc.)  |
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


**Note:** By grouping the data by `ORDERNUMBER`, it is noted that `total orders` < `number of rows`.
This fact, along with the fact that no dublicate rows were found, indicates that each product purchased in an order, is listed in a different row than the other ones, with the `ORDERLINENUMBER` column indicating the way that the products were placed in the order.


**IΙ. Univariate Analysis**

1. **Missing values** and **frequencies** for some of the categorical variables.

The number of rows of the dataset is 2823 while by grouping the data by `ORDERNMUBER`
Since total orders < number of rows, then this means that each product purchased in an order is listed in a different row than the other ones, with the ORDERLINENUMBER column indicating the way that the products were placed in the order.
    
2. Discriptive statistics for some of the numerical variables at the **order item-level** (row-level).
    
3. Discriptive statistics for some of the numerical variables at the **order-level**.
    
4. **Extreme outliers** in item sales.
    
**IIΙ. Multivariate Analysis**

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
