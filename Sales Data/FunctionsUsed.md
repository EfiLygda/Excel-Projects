# Functions Used

Bellow is a detailed presentation of all the Excel 365 functions used in the project:

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
