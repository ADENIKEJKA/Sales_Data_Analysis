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

### Data Visualization
![TOTAL SALES BY PRODUCTS   REGION](https://github.com/user-attachments/assets/77a628d4-5f92-4ac7-aa9c-1ea874a13a6c)

![MONTHLY REVENUE REPORT](https://github.com/user-attachments/assets/b23975b9-6ee3-42a5-8888-1c95dcbdacc3)

![Sales Data Analysis Project 1](https://github.com/user-attachments/assets/5774ed92-6ec8-4efb-9a13-3f6f272905f3)

![SALES PERFORMANCE ANALYSIS FOR RETAIL STORE](https://github.com/user-attachments/assets/0b184e36-c68b-4caa-b7d2-8e6b5d86352c)

### Inferences
1. Top-Performing Regions:
- The South has been the store's strongest market, as seen by the largest revenue made there. This indicates a strong level of client engagement and demand in this location, which may be brought on by seasonal preferences, successful local marketing, or advantageous demographics.
- Although sales in the East region are high, there is still opportunity for development to catch up to the South. Examining Eastern consumers' buying patterns may highlight distinctive product preferences that could be capitalized on.
- The fact that the North and West regions lag behind suggests that these areas may require calculated measures to increase sales. Increased market share in these areas could be achieved, for example, by customized marketing campaigns, focused promotions, or even a closer examination of regional competitors.




