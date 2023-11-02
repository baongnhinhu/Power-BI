# Create a Data Model for Seven Sages Brewing Company

## Project Description:
The objective is to manage the datasets and establish an effective data framework for a small brewery, enabling them to gain deeper insights into their popular and profitable products. This will facilitate informed decision-making regarding product prioritization as the company expands. The project showcases proficiency in fundamental data modeling principles, encompassing data cleansing, organization, and structuring using Power Query, the creation of a date table, building a data model with suitable relationships and filters, and crafting a straightforward report with commonly used visualizations and DAX measures.<br>

Here is a brief overview of the project steps.

### Step 1: Get data
Use files are `CFO Metrics Tracker.xlsx`, `Customer List (as of FY2021).txt`, `SSBC Product Offerings.pdf`, `USD-CAD Exchange Rates.csv`, `Monthly Sales Logs/` downloaded from Udacity and can be found on Datasets/ folder on this repo.

### Step 2: Structure, Combine, and Clean the Data
In this step we will use Power Query to make data cleaning/pre-processing on our datasets:
- Combining the 12 monthly sales files into `Full 2021 Sales` query for analysis.
- Merging` Customer List (as of FY2021).txt` and `SSBC Product Offerings.pdf` to `Product_CP`
- Promoted first rows as headers.
- Renamed queries and columns with suitable names.
- Changed columns' data types
- Removed NULL values in all datasets

### Step 3: Create Your Date Table

You'll need to create a continuous table that covers each full calendar year in the sales data set (starting on January 1st and ending on December 31st. In addition, the table should include:
- Calendar month name and number
- Calendar year
- Fiscal period
- Fiscal year
- Fiscal quarter -Quarter - FY (e.g., Q1 - FY2021)
  
*Note:* Seven Sages' Fiscal year begins on October 1st and runs until September 30th. A transaction on Sept 20th 2020 would fall in FY 2020, but a transaction on October 20th would land in FY 2021

### Step 4:  Build Relationships Between Tables
We created one Face Table `Monthly Sales Log` with four diminsion tables pointing towards it with an active one to many relationship like the screenshot below:
![modelproject 1](https://github.com/baongnhinhu/Power-BI/assets/82852784/9e3f82b7-8ce3-46b5-a43f-9b02176c7310)

### Step 5: Write Your Measures
To satisfy the CFO's requirements, we will need to calculate Sales, Cost of Sales and Gross Profit Margin in two different currencies.
- Sales in USD ($)
- Cost of Sales USD ($)
- Gross Profit Margin (or GPM) in USD (%)
- Sales in CAD ($)
- Unit Sales by Product (%)
- Share of gross profit by Product type (%)

### Step 6: Create a Report
Next we just need to create a visualization to summarize the output of your data model for the CFO. 
In order to meet the CFO's demands, our fundamental report version will consist of two tabs. One tab will provide a summary of sales data categorized by customer and customer type across quarters, labeled one as `Sale and GM`. The second will simply summarize the percentages of gross profit and unit sales by product and would be labeled `Gross Profit and Unit Sales`. Both tabs feature a concise executive summary at the bottom.



