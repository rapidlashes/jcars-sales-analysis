## PREREQUISITES

Raw `csv` file data was first imported to my postgres SQL database then the database connected to my visualization tool (power BI).
The postgres SQL Im using here is cloud based from Aiven.
The tool I used to import this csv file to my Aiven postgres SQL database is dbeaver version 26.1.0
Now since my database is connected to power BI, I just imported the csv file from power Bi and started working on it, another opption was to Direct querry the data but I did not go for that, so my csv file remains untampered in my database.

## CLEANING

Removed duplicates, changed the date columns from text format to date format using locale (English:United Kingdom).
Age column cleaned too, removed the (-) sign from individual ages.
Maintained the Age column in the text format(Age deosnt change through out)
All columns that have prices were converted into whole numbers for them to be able to be querried arithmetically

## KPI'S AND DASHBOARD
When finding the leadtime in days between order date and delivery date , some orders had their order date higher than delivery date so the negatives in the resulta were ignored by using the `ABS()` function 
Slicers for Region, Branches, Car make and Vehicle year were added to make the dashboard more interactive
KPI cards included were for total revenue, total orders, profit margins and leadtime days
Recommendations and insights touching different areas of the analysis like Branches, Sales Representative, Regions and car makes were derived from the Dashboard interaction

## WEB FILE AND REPORT EMBEDDING
PPublished the report on to the power BI service then embedded it into a simple `html` web portal

