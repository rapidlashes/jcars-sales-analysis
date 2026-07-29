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

<img width="931" height="528" alt="Screenshot (228)" src="https://github.com/user-attachments/assets/54ff822c-a9bb-4de4-8762-5fb6332d9ecf" />


***Revenue visuals***

<img width="1223" height="676" alt="Screenshot (227)" src="https://github.com/user-attachments/assets/d1d2ae73-7c9b-42d5-9529-94439c7ce6ef" />

<img width="1259" height="722" alt="Screenshot (225)" src="https://github.com/user-attachments/assets/dbc31289-3df1-419a-bf2e-12b59789b22e" />

***Sales Rep analysis***

<img width="937" height="355" alt="Screenshot (230)" src="https://github.com/user-attachments/assets/8820a228-e0f4-4e92-8cee-a0514e8a01a6" />

***Delivery time***

<img width="1214" height="387" alt="Screenshot (224)" src="https://github.com/user-attachments/assets/26eb612d-9f28-4547-963f-0c15e14d95cd" />


***Insights***

<img width="1146" height="547" alt="Screenshot (223)" src="https://github.com/user-attachments/assets/2cc223f2-6453-4582-af82-0e2f099b8753" />


***Recommendations***

<img width="872" height="567" alt="Screenshot (222)" src="https://github.com/user-attachments/assets/0bc0ec97-2a36-4867-9a42-11687d54f4b4" />


***Dashboard***

<img width="1231" height="721" alt="Screenshot (221)" src="https://github.com/user-attachments/assets/af0c8c6f-ec5d-4336-a431-82fe41797589" />



