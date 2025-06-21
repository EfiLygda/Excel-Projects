# Datailed Results

Bellow the insights from the questions are presented in detail.

-------------------

## **I. Indroduction to the Dataset**

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


> [!NOTE]
> - By grouping the data by `ORDERNUMBER`, it is noted that `total orders` < `number of rows`.
>  This fact, along with the fact that no dublicate rows were found, indicates that each product purchased in an order, is listed in a different row than the other ones, with the `ORDERLINENUMBER` column indicating the way that the products were placed in the order.
> - There are discrepancies when calculating `SALES` as `QUANTITYORDERED * PRICEEACH`, since prices > 100 in `PRICEEACH` column are capped at 100, as per the [this discussion](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data/discussion/82824#1188157) on the dataset.


## **IΙ. Univariate Analysis**

#### 1. **Missing values** and **frequencies** for some of the categorical variables.

- All observations in the dataset include relevant data, with most missing values occuring for the second adress line, state and then postal code.

- The vast majority of orders are shipped (93,16%), with a minority of them in process, cancelled, on hold, resolved or disputed.

- The most frequently ordered products belong to the Classic Cars, Vintage Cars, and Motorcycles product lines. More data would be needed to inferre if these products are for personal use.

- When beaking down the orders's count by region the majority of orders are placed from Europe followed closely by North America. However, breaking down the orders's count by country, the majority are placed from USA.

- Most orders do not list a state, but for USA based clients most orders were placed from California.

- Madrid, Spain is the most frequent city by order count, with 31 orders recorded. This aligns with the broader trend of significant European participation in orders.

    
#### 2. Discriptive statistics for some of the numerical variables at the **order item-level** (row-level).

- Removal of Cancelled, On Hold and Disputed orders was done, in order to analysize the variables.

- The average quantity ordered (QUANTITYORDERED) for each item in an order is approximately 34,93 ± 9,36 units.
The distribution appears to be approximately symmetric (skewness ≈ 0,24), but with a slight platykurtic shape (kurtosis ≈ -0,08), indicating a flatter shape with light tails, thus suggesting slightly less prone towards outliers distribution, compared to the normal distribution.

- The average unit price (PRICEEACH) for each item in an order is approximately 83,64 ± 20,24 currency.
The distribution appears to be moderately to highly left-skewed (skewness ≈ -0,94), due to the fact that, as per the dataset's author's comments, prices over 100 are capped at 100 currency causing most of the prices to crowd at the upper end of the distribution.
It also appears to have a slightly platykurtic shape (kurtosis ≈ -0,39), indicating a flatter shape with lighter tails, thus suggesting it is slightly less prone to outliers, compared to the normal distribution.

- The average sales (SALES) for each item in an order is approximately 3544,38 ± 1819,72 currency.
The distribution appears to be highly right-skewed (skewness ≈ 1,12), indicating a tendency for a few higher priced sales to pull the mean upwards.
It also appears to have a highly leptokurtic shape (kurtosis ≈ 1,50), suggesting it is peaked and more prone to outliers, compared to the normal distribution.

- The average Manufacturer's Suggested Retail Price (MSRP) for each item in an order is approximately 100,89 ± 40,44 currency.
The distribution appears to be moderately right-skewed (skewness ≈ 0,58), indicating a tendency for a few higher priced units to pull the mean upwards
It also appears to have a slightly platykurtic shape (kurtosis ≈ -0,15, suggesting it is flatter and lightly less prone to outliers, compared to the normal distribution.

- Since on average MSRP > PRICEEACH, then that means that the business on average sells bellow the full price of each product.


    
#### 3. Discriptive statistics for some of the numerical variables at the **order-level**.

- Removal of Cancelled, On Hold and Disputed orders was done, in order to analysize the variables.

- The average quantity ordered (QUANTITYORDERED) for each order is approximately 320,91 ± 174,88 products.
The distribution appears to be approximately symmetric (skewness ≈ 0,08), but with a highly platykurtic shape (kurtosis ≈ -1,02) indicating a flatter shape with lighter tails, thus suggesting it is less prone to outliers, compared to the normal distribution.

- The average total unit price (PRICEEACH) in each order is approximately 768,37 ± 418,08 currency.
The distribution appears to be approximately symmetric (skewness ≈ 0,00), but with a highly platykurtic shape (kurtosis ≈ -1,14) indicating a flatter shape with lighter tails, thus suggesting it is less prone to outliers, compared to the normal distribution.

- The average sales (SALES) for each order is approximately 32559,38 ± 17691,56 currency.
The distribution appears to be approximately symmetric (skewness ≈ 0,03), but with a moderately to highly platykurtic shape (kurtosis ≈ -0,93) indicating a flatter shape with lighter tails, thus suggesting it is less prone to outliers, compared to the normal distribution.

- The average Manufacturer's Suggested Retail Price (MSRP) for each order is approximately 926,84 ± 509,24 products.
The distribution appears to be approximately symmetric (skewness ≈ 0,01), but with a platykurtic shape (kurtosis ≈ -1,06) indicating a flatter shape with lighter tails, thus suggesting it is less prone to outliers, compared to the normal distribution.

- Since on average MSRP > PRICEEACH, then that means that the business on average sells bellow the full price of each order.

- Comparing the analysis done at the item-level with the analysis done at order-level, the distributions at the order level appear more robust  by being generally more symmetric and significantly less prone to outliers.


    
#### 4. **Extreme outliers** in item sales.

- Using Z-score to identify outliers, 30 item sales were found. All of them were in the upper end of sales.
- Using Interquartile Range to identify outliers, 81 item sales were found. All of them were in the upper end of sales.
- On average, using both methods, outliers are in the upper end of sales and quantity. 

    
## **IIΙ. Multivariate Analysis**

### **A. Seasonality**
  
#### 1. Quick summary of **total item sales** over the years by each **quarter**.
    
#### 2. Average **monthly discount rate** for each **product line**.
    


### **B. Sales and Revenue**
  
#### 1. Top 5 **countries** and **regions** that generate the **most revenue** from purchases.
    
#### 2. **Average order value** by **country**.
    
#### 3. Top 10 **countries** by **order volume**.
    


### **C. Customer Behaviour**
  
#### 1. Top and bottom 5 **customers** by **orders** placed.
    
#### 2. Top and bottom 5 customers by **average individual** order item **sales**.
    
#### 3. **Countries** sorted from the highest to least amount of **return customers**.
    
#### 4. Most popular **product lines** by **region** and **country**.
    


### **D. Product-Level Analysis**
  
#### 1. Top and bottom 10 **most ordered products**.
    
#### 2. Top and bottom 5 **products** by **order volume**. 
    
#### 3. Top **product lines** based on **total sales**.
    
#### 4. **Average discount rate** per **country** and **region**.
