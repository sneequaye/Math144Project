# Math144Project

## Motivation
As an aspiring public health professional, I am interested in factors that can be used to improve population health. Access to green space stood out to me because I recently took up running over the summer because the area where I lived, had an actual running trail which made t convenient do it close to home. This made me wonder whether in areas more densely populated and had less green space, made people less likely to take up hobbies like running due to the lack of infrastructure in their neighborhood. Hence, for this personal dataset project I decided to explore how access to green space may affect health outcomes in New York State specially looking at obesity. 

## Data Sources

I got my data from the [CDC National Environmental Public Health Tracking Network]([url](https://ephtracking.cdc.gov/DataExplorer/)) and the [New York Behavioral Risk Factor Surveillance System]([url](https://www.health.ny.gov/statistics/prevention/injury_prevention/information_for_action/docs/2023-03_ifa_report.pdf)) (BRFSS). The green space data was recorded for 2020 while the New York State obesity rate data was recorded for 2021 yet released in 2023.

## Processing Steps
On the CDC website mentioned, I went through the query panel and completed each step with the data I wanted. For Step 1(Content Area), I selected "Built Environment". For the Indicator I selected Access to Parks and Public Elementary Schools. For measure I selected Percent of People living within 1/2 or 1 mile of a park. For Step 2 Geography Type, I selected "State by County". For Step 3 (Geography), I selected New York. For Step 4 (Time), I selected 2020. And for Step 5 (Advanced Options) I selected 1/2 Mile for "Distance to Parks". I chose not to include race demographics. I then downloaded the data and uploaded it to an Excel spreadsheet

For the BRFFS Data, since it was a pdf, I created my own table in google docs and inputted the data manually. I then copied the table and added it to the Excel Spreadsheet that contained the green space data.

In terms of cleaning the data, I renamed some columns for easier readibility. So the "Value" column which contained the green space percentage, I changed to "greenspace". The column that contained the obesity rate data i changed from "Percent.of.adults.who.have.obesity...." to "obesity"
Also the Green space data was being read as a string in R since it was already in percentage format. To convert the percentages into numerical data, I had to transform the columns into decimals.

In order to carry out the analysis below, I removed some columns that were mostly empty or didn't have interesting information and condensed some of the columns that had too many classes. I also added a couple of binary columns (kids and math) to make some of the analysis easier. The transformed data is uploaded here, along with the processing script. 

## Visualization
<img width="1400" height="865" alt="image" src="https://github.com/user-attachments/assets/9856b4cf-35c8-4fa8-b356-16a865dabd25" />
<img width="1400" height="865" alt="image" src="https://github.com/user-attachments/assets/4aad4270-d159-4b25-930f-86d3fb27c1df" />


## Analysis
<img width="1400" height="865" alt="image" src="https://github.com/user-attachments/assets/40113be9-68ba-4cff-b368-7ea46019f366" />

