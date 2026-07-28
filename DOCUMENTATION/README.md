## PREREQUISITES

Raw csv file data was first imported to my postgres SQL database then the database connected to my visualization tool (power BI).
The postgres SQL Im using here is cloud based from Aiven.
The tool I used to import this csv file to my Aiven postgres SQL database is dbeaver version 26.1.0
Now since my database is connected to power BI, I just imported the csv file from power Bi and started working on it, another opption was to Direct querry the data but I did not go for that, so my csv file remains untampered in my database.

## CLEANING

Removed duplicates, changed the date columns from text format to date format using locale (English:United Kingdom).
Age column cleaned too, removed the (-) sign from individual ages.
Age column converted into numeric, blank customer  age values and ages less than 10 were flagged 
All columns that have prices were converted into whole numbers for them to be able to be querried arithmetically
Calculated the column for Delivery time which was (delivery date - order date), used the return function to return only values that are positive. All negative values were converted to blanks so that they dont affect arithmentic functions like `AVG()`, `SUM()`, `MAX()`, `MIN()` associated with this column.

## KPI'S AND DASHBOARD
All KPI visuals were filtered with the age validity, rendering the flagged age values invalid and excluding them from being querried. The flagged values are later to be investigated.

## SCREENSHOTS

***KPI cards***



***Revenue visuals***



***Insights***



***Recommendations***


***Dashboard***



