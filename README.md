# Myseller Global Sales

### Project Overview
 Mysellar, a multinational retail corporation that operates a chain of stores – online and offline – in all continents. The items sold cut across a range of categories including cosmetics, baby food, household, office supplies, and clothes.
Mysellar wants to use its sales data to inform decision-making on the profitable products to focus on and which markets to concentrate sales efforts on, using historical data to perform descriptive analysis and present valuable insights to guide Mysellar’s sales operations. 

![Myseller Dashboard Pic](https://github.com/user-attachments/assets/58ccd7fb-ea3a-49c9-88b6-75df1904b1ac)


### Data Sources
Myseller Global Sales Data: The primary dataset used for this analysis is the " Mysellar Global Sales.xlsx" file, containing detailed information about each Myseller Global Sales from 2019-2021.

### Tools
-	Microsoft Excel – Data Cleaning
- Power BI – Data Visualization/Cleaning

### Data Cleaning/Preparation
 In preparing this data properly, we carried out the following tasks:
-	Data loading and inspection.
-	Removing irrelevant cells and colours
-	Handling missing and duplicate values
-	Data cleaning and formatting
-	Getting a data from a Web source and formatting it.

### Exploratory Data Analysis (EDA)
EDA involved in exploring Myseller Global Sales data to answer key questions, such as:
1.	What is the total yearly profit for each sales channel – online and offline?
2.	Show the total units sold per region.
3.	Have the sales of any category of the product increased or decreased over time?
4.	Show the monthly trend of sales and profit in 2021. What are the top-performing regions in terms of revenue and profits?
5.	What is the average shipping time (days) and which region has the lowest average number of days it takes to ship orders?
6.	What are the top 5 and bottom 5 countries by order volumes?
7.	An executive is postulating that Mysellar should be generating more sales in countries with higher economic productivity. For countries in Sub-Saharan Africa, is there a correlation between total sales and GDP? Highlight countries of interest in your report.

### Data Analysis

The analysis includes some interesting DAX measures such as;
```Plain text
Total_Revenue = SUM('MySeller Cleaned Data_Sheet'[Total Revenue])
Profit = CALCULATE([Total_Revenue]-[Total_Cost]) 
Profit Margin = DIVIDE([Profit],[Total_Revenue],0) 
Online Sales Channel Profit = CALCULATE([Profit],'MySeller Cleaned Data_Sheet'[Sales Channel] = "Online")
Offline Sales Channel Profit = CALCULATE([Profit],'MySeller Cleaned Data_Sheet'[Sales Channel] = "Offline")
Avg_Shipping_Days = PERCENTILEX.INC('MySeller Cleaned Data_Sheet', 'MySeller Cleaned Data_Sheet'[Shipping Duration], 0.5) &  "Days"
```

### Results
The analysis results are summarized as follows:
-	Office Supplies is the category with highest revenue yearly while Fruits is the lowest.
-	Based on the unit sold by Region, Europe ranks the highest (24.03%) followed by Sub-Saharan Africa (23.19%) while North America is the lowest (1.95%).
-	There was an increase in profits and revenues in January of 2021 while there was significant decrease in February and March of the same year.
-	There were more sales through Online Sales Channels compared to the Offline Sales Channels.
-	Sub-Saharan Africa generated more revenues than any other Region while North America is the lowest.

### Recommendations
From the analysis, we recommend the following actions:
-	Since Online Sales Channels generates more income, Myseller, should focus more on the Online Sales while building up that of Offline Sales in order to make more profits.
-	There was significant decrease in profits and revenues in 2020 and 2021 which might be due to COVID-19 and post COVID-19 economic instability, we recommend that that Myseller should do some promotions, adverts, 
and discounts to raise awareness for the members of the public.
-	In North America where there are lowest sales of Myseller Products, Myseller should figure out salable products in the region and invest more in it.

### References
•	A lookup table for nominal GDP is provided [Download Here](https://en.wikipedia.org/wiki/List_of_African_countries_by_GDP_(nominal))



