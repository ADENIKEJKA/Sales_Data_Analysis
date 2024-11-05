# Sales_Data_Analysis

### Project Title: Sales Analysis for A Retail Store

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Inferences](#inferences)

### Project Overview
---
The purpose of this data analysis project is to provide insight into a retail store's sales performance from 2023 to 2024. We want to obtain sufficient understanding to make rational judgments by analyzing the different parameters in the acquired data, which then allows us to create engaging narratives around our data.

### Data Sources
---
The primary source of this data was provided by the retail store based on infromation gathered as regards their various customers and saved in an excel sheet.

### Tools Used
---
- MIcrosoft Excel; [Download here](https://www.microsoft.com)
  1. For Data Cleaning
  2. Analysis
  3. Visualization
 
- SQL - Structured Query Language for Querying of Data
- GitHub for Portfolio building
- Power BI for Data cleaning, Analysis and Presentation

### Data Cleaning and Preparations
---
The following tasks were carried out during the first stage of data cleaning and preparations:
1. Data loading and examination
2. Removal of Duplicate information in the data
3. Formatting and data cleaning

### Exploratory Data Analysis
---
EDA entailed examining the data to uncover key insights, such as:
-What are the Top-selling Products?
-What are the monthly sales trends?
-What are the sales performances in the regions?

### Data Analysis
---
This is where we included some basic lines of code or queries and some of the DAX expressions used during the analysis;
```SQL
Select Product, SUM(REVENUE) AS TotalSales 
from [dbo].[SALESData]
group by Product

Select Region, Count(*) AS NumberOfSalesTransaction 
from [dbo].[SALESData]
group by Region

Select Top 1 Product, SUM(Revenue) AS HighestSellingProduct
from [dbo].[SALESData]
group by Product

SELECT
      FORMAT(OrderDate, 'yyyy-MM') AS Sales_Month,
	  SUM(Revenue) AS Monthly_Sales_Total
FROM  [dbo].[SALESData]
WHERE YEAR(OrderDate) = 2024
GROUP BY 
       FORMAT(OrderDate, 'yyyy-MM')
ORDER BY 
      FORMAT(OrderDate, 'yyyy-MM')
```
