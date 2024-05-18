# Week_3 - Florida Crime Statistics
### *Authored Alex Lopez & Katherine Granados*
This project analyzes Florida Crime Reporting data from the Florida Department of Law Enforcement 
through two reporting sources: The Florida Convictions History Dashboard and 
the Florida Incident-Based Reporting System. 

For the datasets, we used the 2023 FIBRS Report and the FLDE Conviction data from 
2019 to 2023

Regarding the datasets;

FIBRS: 

- Had header columns which proved difficult to manipulate when including them as multi-indexed columns
- With over 200 rows of data broken down by quarters, it was ultimately chosen to drop many columns 
  keeping the year to date section per each crime, bringing column count down to 40
  
FDLE:	  
- This dataset was a great data source for the questions we posed. 
  There weren’t any null values within the columns we were interested in. 
  This dataset provided much needed insight and was clear to read, 
  therefore easier to utilize.
	  
We wanted to answer the following questions: 
- Was Miami-Dade County among the top 10 counties with most occuring crime incidents?
- Was there a significant drop off in crime in 2020, coinciding with Covid-19 Lockdown,
  with a trend upwards back to or above 2019 levels.
  
We analyzed the data through these criteria:
- Counties with the most incidents over the past 5 years (FDLE)
- Most common reported crime incidents over the past 5 years (FDLE) 
- The top reported type of crime incident per year in each county (FDLE)
- The most common grouped types of crime incidents across Police Departments 
  in Miami Dade County (FIBRS)

For our data cleaning, we did the following: 
- Retained columns selectively instead of dropping them (40 out of 232 columns) (FIBRS)
- Used optional argument “skiprows” in read_excel to only get columns and 
  not have multi-indexed columns (FIBRS)
- Developed a function to identify top crimes for each county-year combination (FDLE)
- Dropped Duplicate Rows and dropped columns with NaNs/weren't of use to us (FDLE)
- Standardized column names to lowercase with underscores for 
  enhanced clarity and conformity to industry standards (FDLE/FIBRS)

In our analysis, we concluded that Miami-Dade was in the top 10 but was lower 
than other counties such as:
- its neighbor Broward County (9)
- The Tampa Bay Aread Pinellas(1) & Hillsborough Counties(2)

We also saw that while there was a dropoff in reported incidents in 2020, 
There was a **Downward** trend after 2021 and 2023 had the fewest reported incidents.
which indicates that 2023 is notable for having the lowest recorded criminal incidents 
in recent years 
 
- Link to source of data set files: 
	- FDLE Florida Convictions: https://www.fdle.state.fl.us/CJAB/FSAC/CJDT-Presentation.aspx
	- FIBRS: https://www.fdle.state.fl.us/CJAB/UCR/Annual-Reports/FIBRS
	
	
	
