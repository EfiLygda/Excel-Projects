# Excel-Projects

## Projects

### Sales Data EDA

An exploratory data analysis (EDA) project focused on understanding sales patterns across customers, regions, and order statuses. 
The analysis was done in `Excel 365`, and leverages descriptive statistics and visualizations to generate insights into pricing, product lines, and sales behavior.
By design, dynamic arrays were mostly used to answer the questions, without relying on traditional pivot tables, except for the use of the `PIVOTBY()` function in one instance.

In [`Sales Data/ReadMe.md`](https://github.com/EfiLygda/Excel-Projects/tree/main/Sales%20Data#sales-data-eda) the details of the project are presented.

---------------------

#### Tools Used

`Microsoft Excel 365`

#### Project Structure

- The whole project is located in workbook `Sales_Data_Project.xlsx`, which contains the following four worksheets:

    - `Table of Contents`: A simple TOC that links to the location of the dataset, each question and the small dashboard included.
    - `Data`: The sales dataset used for the analysis.
    - `S1. Answers`: Contains the answers to the questions for the analysis.
    - `S2. Small Dashboard`: Contains a small dashboard providing a quick summary of the product lines by each order status

- In [`DetailedResults`](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/DatailedResults.md#datailed-results) the questions and the detailed insights infered from the data are located.

- In [`FunctionsUsed`](https://github.com/EfiLygda/Excel-Projects/blob/main/Sales%20Data/FunctionsUsed.md#functions-used) the Excel 365 functions used in the project are presented, in detail.


> [!NOTE] 
> The dataset used in this project is licensed under the [CC BY-NC-SA 3.0 license](https://creativecommons.org/licenses/by-nc-sa/3.0/) and is available at [Kaggle](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data/data).


## Functions Used

The functions used were mainly for:
- **Math & Statistics** calculations and aggregations (`AVERAGE/AVERAGEIFS`, `STDEV.S`, `SKEW`, `KURT` etc.)
- Usage of **Dynamic Arrays & Sorting** (`SORT`, `UNIQUE` etc.)
- **Flexible retrieval** of values (`FILTER`, `VLOOKUP`, `INDEX`, `MATCH` etc.)
- **Data Grouping & Aggregation** (`GROUPBY/PIVOTBY`)
- **Enabling procedural-style programming within Excel formulas** (`LET`, `MAP`, `LAMBDA` etc.)
- **Text Manipulation** (`TEXTJOIN`, `MID` etc.)

## Licensing

- This repository is under the MIT License.
- The dataset in the `Sales Data/` folder is under the [CC BY-NC-SA 3.0 license](https://creativecommons.org/licenses/by-nc-sa/3.0/).
