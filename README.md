
# Power BI Sales Analysis Dashboard

A brief description of what this project does and who it's for

# Sales-Dashboard


## Problem Statement

TechnoEdge company has provided  a dataset that includes various tables such as Calendar, Customers, Product Categories, Product Sub-Categories, Products, Returns, Territories, and Sales from 2022-2024. The purpose of analyzing this dataset is to gain insights and improve business operations. Using DAX Power BI, we can create interactive reports and visualizations to analyze sales trends, customer behavior, product performance, and returns. This will help in making data-driven decisions and improving business profitability.


## Objectives
1) To analyze sales data for TechnoEdge company across different regions, countries, and product categories.

2) To identify trends and patterns in sales data that can help improve business performance.

3) To understand customer behavior and preferences based on their buying patterns.

4) To identify high-performing products and product categories, as well as underperforming ones.

5) To monitor key sales metrics such as sales, profit, and profit margin, and identify areas for improvement.

6) To create reports and visualizations that can help stakeholders make informed decisions about sales and marketing strategies.

Overall, the objective of the TechnoEdge sales dataset is to provide valuable insights into the company's sales performance and help identify areas for improvement, so that the company can optimize its sales and marketing strategies and improve its bottom line.

## Steps

### Data Modelling

Creating a relationship between tables in the model view of Power BI using a common column improves the accuracy and reliability of data analysis and visualization.

### Data view

Display all geographical datasets in Power BI along with their corresponding data categories, such as city, country, state, and region.


### DAX Functions

Date Functions

![Age Group](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/f521cc3e-e5c1-47bc-b31c-2ab13fb75f01)

![AgeDiff](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/ac99edbc-9f2a-4780-b76b-0512d9e6c06c)

![DAX Commands](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/9ac7851f-5fcc-4581-a95a-b65c41bf4104)

![DAX Fiscal Year](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/c6d71197-1fd7-4e2b-b550-7082841f32f7)

![DAX Quarter Q](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/7e1c6085-809a-4a05-9fee-77c79dcf56f2)

![Dax Month Format](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/80423639-4a62-4265-aa8d-7c1adcd1ee79)

![Dax startof month](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/5a547051-f892-444c-beab-78334f492843)

![Last 6 Months](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/515c77cb-a561-4970-8796-dee527981c45)

![Yearly Quarter](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/8280c671-3833-4414-8317-00f1e3d6a86c)

Text Functions

DAX Function	Full Name = Customers_Dim[Prefix] &" "& Customers_Dim[First Name] &" "& Customers_Dim[Last Name]

Calculate Functions

	2022 = CALCULATE([Total profit],Calendar_Dim[Year]="2022",YEAR(Calendar_Dim[Date]=2022))
	
	2023 = CALCULATE([Total profit],Calendar_Dim[Year]="2023",YEAR(Calendar_Dim[Date]=2023))
	
	2024 = CALCULATE([Total profit],Calendar_Dim[Year]="2024",YEAR(Calendar_Dim[Date]=2024))

Aggregation Functions

Total Order = SUM(Sales_Fact[OrderQuantity])

Total return No = COUNT(Returns_Fact[ReturnQuantity])

Total order-NO = DISTINCTCOUNT(Sales_Fact[OrderNumber])

DAX Function	Total Revenue = SUMX(Sales_Fact,Sales_Fact[OrderQuantity]*related(Products_DIM[ProductPrice] ))

DAX Function	Total Cost = SUMX(Sales_Fact,Sales_Fact[OrderQuantity]
	*related(Products_Dim[ProductCost])

DAX Function	SUMMARIZE = SUMMARIZE (Territories_DIM,Territories_DIM[Country],"Profit",[Total profit])
	
Total profit = [Total Revenue]- [Total Cost]

### File Download Link

https://easyupload.io/wohx6v

        
Report Snaps ,

![Capture](https://github.com/Sagarbhar/Power-BI-Sales-Analysis-Project-DAX-/assets/168229258/463b0a55-e63d-4702-9246-988348adf73d)

    
