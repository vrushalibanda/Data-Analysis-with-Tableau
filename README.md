# Data-Analysis-with-Tableau
Learning Objectives
1.	Data Extracts: How to create, when is it appropriate to use?
2.	Table calculations, Year over Year Growth Calculations
3.	Reference lines and bullet graphs for monitoring performance
4.	Filtering based on ranks. Identifying leading and lagging performers

Instructions
1.	Data Source
a.	FactSales, Channel, Date, Product and Subcategory, Category, Store and Geography, Promotion
b.	Create Custom SQL (Data-> Covert to Custom SQL)
c.	Remove unnecessary attributes
d.	Change to Extract
e.	Add filters to extract: Year =2008 to 2009, Region = United States, State = Washington, Channel =Store
2.	Create Sheet: Sales Growth YoY
a.	Create Product Category Hierarchy
b.	Use Category Hierarchy as Rows, DateKey as columns and expand to quarters, Sales Amount as Cell values
c.	Select Sum(Sales Amount) from Marks panel and select Add Table Calculation. Select Percent Difference From as Calculation Type, Dimension for Compute Using , and Check Year as Dimension.  The sheet should show growth in sales from previous year.
3.	Create Sheet: Targets by Category
a.	Create calculated columns 
i.	YR 2008 Sales Amount: IF [Calendar Year] = 2008 THEN [Sales Amount] END
ii.	YR 2009 Sales Amount: IF [Calendar Year] = 2009 THEN [Sales Amount] END
b.	Create Bullet graph with Product Categories as dimension, 2009 and 2008 sales as measures, right click on the vertical axis to swap reference from 2009 to 2008
4.	Create new sheet: Top Selling Products
a.	Create calculated field profit as Sales Amount – (Total Cost + Return Amount)
b.	Create calculated field to rank products that exceed 2008 sales targets
i.	RANK(SUM([YR 2009 Sales])-SUM([YR2008 Sales]))
c.	Use Product Names as Columns and Sales 2009 and Sales 2008, and Profit as measures 

