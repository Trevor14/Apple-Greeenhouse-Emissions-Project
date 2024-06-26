# Apple-Greeenhouse-Emissions-Project
The focus for this analysis was to showcase Apple’s incredible journey in all aspects of their corporate business and their commitment to be carbon neutral, contributing towards the SDG Goal 13 Climate Action, throughout the life of their products towards achieving their 2030 goals. My project involved visualizing their progress towards becoming carbon neutral by 2030 using data generously provided by Apple in their Environmental Progress Report.

After announcing that its company's operations were carbon-neutral by 2020, Apple made a commitment to make its products carbon-neutral by 2030. To achieve this goal , they set their emissions (38.4 million metric tons of CO2e) as a starting point for 2015, to reduce and target 75% by 2030. All emissions will be offset by carbon offsets of the remaining 25% (9.6 million metric tons of CO2e) has been eliminated, bringing emissions to zero.


DATA ANALYSIS EXPRESSIONS.

1. Total Revenue = SUMX(normalizing_factors,normalizing_factors[Revenue])

2.Total Market capitalization = SUMX(normalizing_factors,normalizing_factors[Market Capitalization])

3.Total Product life cycle Emissions = CALCULATE(SUM(greenhouse_gas_emissions[Emissions]),'greenhouse_gas_emissions'[Category]="Product life cycle emissions")

4.Total Gross Emissions = CALCULATE(SUM(greenhouse_gas_emissions[Emissions]),'greenhouse_gas_emissions'[Type]="Gross Emissions")

5.Total Greenhouse Emissions = SUM(greenhouse_gas_emissions[Emissions])

6.Total Corporate Emissions = CALCULATE(SUM(greenhouse_gas_emissions[Emissions]),'greenhouse_gas_emissions'[Category]="Corporate Emissions")

7.Total Carbon Removals = CALCULATE(SUM(greenhouse_gas_emissions[Emissions]),'greenhouse_gas_emissions'[Type]="Carbon Removals")

8.Revenue Growth Rate - YoY =  VAR CurrentYearRevenue = SUMX(FILTER('normalizing_factors', 'normalizing_factors'[Fiscal Year] = MAX('normalizing_factors'[Fiscal Year])), 'normalizing_factors'[Revenue]) VAR PreviousYearRevenue = SUMX(FILTER('normalizing_factors', 'normalizing_factors'[Fiscal Year] = MAX('normalizing_factors'[Fiscal Year]) - 1), 'normalizing_factors'[Revenue]) RETURN DIVIDE(CurrentYearRevenue - PreviousYearRevenue, PreviousYearRevenue) 

9.Market Capitilation Growth Rate - YoY =  VAR CurrentYearMarketCapitilation = SUMX(FILTER('normalizing_factors', 'normalizing_factors'[Fiscal Year] = MAX('normalizing_factors'[Fiscal Year])), 'normalizing_factors'[Market Capitalization]) VAR PreviousYearMarketCapitilation = SUMX(FILTER('normalizing_factors', 'normalizing_factors'[Fiscal Year] = MAX('normalizing_factors'[Fiscal Year]) - 1), 'normalizing_factors'[Market Capitalization]) RETURN DIVIDE(CurrentYearMarketCapitilation - PreviousYearMarketCapitilation, PreviousYearMarketCapitilation) 

10.Employees Growth Rate - YoY =  VAR CurrentYearEmployees = SUMX(FILTER('normalizing_factors', 'normalizing_factors'[Fiscal Year] = MAX('normalizing_factors'[Fiscal Year])), 'normalizing_factors'[Employees]) VAR PreviousYearEmployees = SUMX(FILTER('normalizing_factors', 'normalizing_factors'[Fiscal Year] = MAX('normalizing_factors'[Fiscal Year]) - 1), 'normalizing_factors'[Employees]) RETURN DIVIDE(CurrentYearEmployees - PreviousYearEmployees, PreviousYearEmployees)

11.Count Employees = sum(normalizing_factors[Employees])

12.Avg carbon footprint = AVERAGE(carbon_footprint_by_product[Carbon Footprint])


Tools Used in the Analysis:
1.Power BI
2.DAX
3.Power Query Editor
4.Power BI Desktop
5.Power BI Dashboard
6.Excel
