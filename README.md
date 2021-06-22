# US-States-GDP-and-Population-Report

## Goals:
* A Power BI report analyzing population and GDP for US states since 1997. Clean and filter the data using Power Query, then create relationships between your tables. Use measures in DAX to calculate growth rates and GDP per capita similar to our approach in the Week 2 videos. Finally, visualize and explore the data in Power BI Desktop.

## Formulas in DAX:
* To find GDP:
 GDP = CALCULATE(SUM(Indicator[Value]))
* To find GDP per Captia:
GDP per Captia = DIVIDE([Population],[GDP],0)
* To find Population:
Population = CALCULATE(SUM('US States Population by Year'[Value]))
* To find GDP Growth
GDP Growth = 
var First_Year = CALCULATE(MIN(Indicator[Year])) 
var Latest_Year = CALCULATE(MAX(Indicator[Year]))
var FirstYearGDP = CALCULATE([GDP], Indicator[Year] = First_Year)
var LatestYearGDP = CALCULATE([GDP], Indicator[Year] = Latest_year)
var Diff = LatestYearGDP - FirstYearGDP
return
DIVIDE(Diff,FirstYearGDP,0)

## Techniques need to use:
* Power Query
* Filtering
* Replace values
* Unpivoting
* Power BI Desktop
* Map visual
* Slicers and/or filters




