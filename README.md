PPREREQUISITES
Raw csv file data was first imported to my postgres SQL database then the database connected to my visualization tool (power BI).
The postgres SQL Im using here is cloud based from Aiven.
The tool I used to import this csv file to my Aiven postgres SQL database is dbeaver version 26.1.0
Now since my database is connected to power BI, I just imported the csv file from power Bi and started working on it, another opption was to Direct querry the data but I did not go for that, so my csv file remains untampered in my database.

CLEANING

Removed duplicates, changed the date columns from text format to date format using locale (English:United Kingdom).
Age column cleaned too, removed the (-) sign from individual ages.
