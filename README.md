# Metro-Data
We were tasked by Robyn Mace (Nashville Metro's first data officer) to clean up and analyze the property standards violations data pulled from https://data.nashville.gov/, and then to correlate this information to existing city codes in hopes of drawing insight into key relationships.  

Main steps in this data problem included the following:
1.  Determine and implement a strategy to reduce the 900+ violation types listed in the spreadsheet "Codes' List of Violations 15 aug 2017.xlsx" to just 20 or so main categories.
2.  Tidy the Property Standards Violations dataset available at https://data.nashville.gov/Business-Development-Housing/Property-Standards-Violations/479w-kw2x so that you have a single observation in each row and a single variable (measurement) in each column. This will allow you to test the efficacy of your coding strategy from step 1.
3.  Perform Exploratory Data Analysis on the Property Standards Violations data to showcase the insight your work has enabled.

The largest take away from this project was just how messy real data can be, which proved to be invaluable experience for me. 
1.  Imported the property standards data using sqlalchemy.  
2.  Explored the actual categories of each obervation. 
3.  Separated each violation noted within a single observation (sometimes containing multiple violations stringed together by ","'s) into it's own obersation within these property standards. 
4.  Established there are 22 separate, unique categories within the "Codes" list and established a dictionary for these categories.  
5.  Created a function to iterate through and property standards violations dataframe and create a new column to add these categories to the dataframe.  
6. Merged the codes and property standard dataframes to create with a concise category column for all observations.  
7. Used bokeh to generate a google maps display of violations noted within Davidson County.  
