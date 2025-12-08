# Math144Project

## Motivation
As someone interested in public health, I wanted to look at environmental factors and their correlation with population health. Access to green space stood out to me because I recently took up running over the summer and the convenience of living near a park with a running trail came in handy. This made me wonder whether people living in areas more densely populated and with less green space, were less likely to take up recreational exercises like running due to the lack of infrastructure in their neighborhood. Hence, for this personal dataset project I decided to explore how access to green space may affect health outcomes in New York State specially looking at obesity. 

## Data Sources

I got my data from the [CDC National Environmental Public Health Tracking Network](https://ephtracking.cdc.gov/DataExplorer/) and the 2021 [New York Behavioral Risk Factor Surveillance System]([url](https://www.health.ny.gov/statistics/prevention/injury_prevention/information_for_action/docs/2023-03_ifa_report.pdf)) (BRFSS). 

## Processing Steps
On the CDC National Environmental Public Health Tracking Network website, I had to go through a query panel to select the specific data I wanted. For Step 1 _(Content Area)_, I selected "Built Environment". For the _Indicator_ I selected "Access to Parks and Public Elementary Schools". For _Measure_ I selected "Percent of People living within 1/2 or 1 mile of a park". For Step 2 _Geography Type_, I selected "State by County". For Step 3 _(Geography)_, I selected New York. For Step 4 _(Time)_, I selected "2020". And for Step 5 _(Advanced Options)_ I selected "Distance to Park: 1/2 Mile". I chose not to include race demographics. I then downloaded the data and uploaded it to an Excel spreadsheet.

For the BRFFS Data, since it was a pdf, I created my own table in google docs and inputted the data manually. I then copied the table and added it to the Excel Spreadsheet that contained the green space data.

In terms of cleaning the data, I renamed some columns for easier readibility. So the "Value" column which contained the green space percentage, I changed to "greenspace". The "Percent.of.adults.who.have.obesity...." got renamed to "obesity". I also deleted columns "County FIPS" and "State Fips" that contained irrelevant data for my analysis.
The Green space data was being read as a string in R since it included the percent sign so I had to convert it to numerical data. 


## Visualization
After performing EDA and observing trends in the data, I narrowed down the top 5 counties with the highest amount of green space and the bottom 5 counties with the lowest percentage of green space. These plots compares counties in the top 5 or bottom 5 and their respective obesity rate.

<img width="1400" height="865" alt="image" src="https://github.com/user-attachments/assets/9aa18291-5384-4f82-baa9-5144b61c657d" />
<img width="1400" height="865" alt="image" src="https://github.com/user-attachments/assets/3ac42f8a-ce7b-4ff9-bbde-11bac0088499" />


## Analysis
The bar charts clearly showed an association with low green space and higher obesity rates and vice versa. So I decided to create a scatter plot of the data to see whether there was a linear relationship between green space and obesity rate by NY County.
<img width="1400" height="865" alt="image" src="https://github.com/user-attachments/assets/40113be9-68ba-4cff-b368-7ea46019f366" />

The regression shows a negative trend revealing that obesity and green space percentages are negatively related. On average, when green space access is low, we can expect obesity rates to be higher. However, this analysis is limited since there may be confounders present such as the COVID-19 Pandemic. This could mean green space wasn't as highly utilized since most people were remaining indoors and obesity rates could be attributed to more people staying home and eating more.

