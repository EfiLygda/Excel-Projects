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

- In [`DetailedResults`](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/Datailed%20Results.md#datailed-results) the questions and the detailed insights infered from the data are located.

## Tools Used

`Microsoft Excel 365`


## Methods

### 1. Data Handling & Preparation

The original `csv` file was converted to `xlsx` using `Microsoft Excel 365`.
There were no dublicates rows using as primary keys the unique order number and order line number for each order, so no rows were removed.
Cancelled, On Hold or Disputed orders were removed from the analysis when revenue was analized, but not when customer behaviour was studied. 


### 2. Analytical Techniques

Descriptive statistics such as `mean`, `median`, `std. dev.`, `skewness` and `kurtosis` were used to study the distributions of numerical variables, identifying skewed variables or heavy tails.
Grouping, aggregation, sorting and ranking was done, when necessary.




### 3. Functions Used

|Group| Function Name |Functionality|
|-----|---------------|-----|
|Math & Statistics|`MAX`/`MIN`|Min/max calculations|
||`SUM`/`SUMIFS`|Used for filtered/non-filtered sum calculations|
||`COUNT`/`COUNTA`/`COUNTIFS`/`COUNTBLANK`|Used for filtered/non-filtered count calculations|
||`AVERAGE`/`AVERAGEIFS`|Used for filtered/non-filtered calculations of averages|
||`STDEV.S`/`MEDIAN`/`SKEW`/`KURT`|Descriptive statistics used for distribution shape evaluation|
||`QUARTILE.INC`|Quartile calculations for outlier detection|
||||
|Logical Functions|`IF`/`IFERROR`|Used for conditional checks|
||`NOT`/`OR`/`ISNA`|Basic logical functions, used primarily along with `IF`|
||||
|Text|`MID`|Used for extracting text|
||`TEXTJOIN`|Used for joining text in ranges, mainly unique values|
||`TEXT`/`VALUE`|Converting to text or numerical, respectively|
||||
|Reference & Lookup|`COLUMNS`/`ROWS`|Used for calculating number of columns or rows|
||`FILTER`/`INDEX`/`TAKE`|Filter table when need, usually used in combination for extracting data|
||`MATCH`|Mainly used for finding exact match, usually in combination with the above functions|
||`VLOOKUP`|Used for finding values vertically of table and extracting the value in the same row but in another column|
||`OFFSET`|Used for automating calculations, when other functions cannot be used|
||||
|Dynamic Arrays & Sorting|`SORT`|Used when sorting (ascending or descending)|
||`UNIQUE`|Used for finding unique values|
||`TRANSPOSE`|Used for transposing|
||`HSTACK`|Used for stacking columns in one table horizontally|
||||
|Data Grouping|`GROUPBY`/`PIVOTBY`|`GROUPBY` is mainly used for grouping, while `PIVOTBY` only is used in III.A.2|
||||
|Programming|`MAP`/`LAMBDA`|Used in combination to map the function defined in `LAMBDA`. Also used with `GROUPBY`|
||`CHOOSE`|Used to build dynamic tables or plots|
||`SEQUENCE`|Used in combination with `INDEX` to slice tables|
||`HYPERLINK`|Used for building Table of Contents|
||`LET`|Mainly used to build complicated formulas. Enables procedural-style programming within Excel formulas.|


   


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



