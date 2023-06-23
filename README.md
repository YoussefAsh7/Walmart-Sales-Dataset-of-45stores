# Project: Retail Analysis with Walmart Data

## Introduction:
This project involves the analysis of historical sales data for 45 Walmart stores located in different regions. The data set covers the period from 2010-02-05 to 2012-11-01 and includes the following fields:

- Store: The store number
- Date: The week of sales
- Weekly_Sales: Sales for the given store
- Holiday_Flag: Whether the week is a special holiday week (1 - Holiday week, 0 - Non-holiday week)
- Temperature: Temperature on the day of sale
- Fuel_Price: Cost of fuel in the region
- CPI: Prevailing consumer price index
- Unemployment: Prevailing unemployment rate

The project aims to explore the relationships between these variables and answer specific questions regarding the sales data.

## Example Questions of Interest:
1. Which store has the maximum sales?
2. Which store has the maximum standard deviation, indicating high variability in sales?
3. Identify holidays with higher sales than the mean sales during non-holiday weeks for all stores together.
4. Provide a monthly and semester view of sales in units and gain insights.
5. Plot the relationships between weekly sales and other numeric features and provide insights.

## Importing Libraries:
The following libraries will be used in this project: pandas, matplotlib.pyplot, seaborn, and warnings.

## Data Import and Display:
The data is read from a CSV file named "walmart-sales-dataset-of-45stores.csv" and stored in a pandas DataFrame called "data". The first few rows of the data are displayed using the `head()` function.

## Data Cleaning:
An overview of the data is obtained using the `info()` function, which shows the column names, data types, and non-null counts. Descriptive statistics of the data are computed using the `describe()` function to get insights into the numerical variables. The presence of missing values is checked using `isnull().sum()` and duplicated rows are checked using `duplicated().any()`.

## Value Distribution:
Histograms and subplots are plotted to visualize the distribution of the data.

## Exploratory Data Analysis:
Several research questions are explored:

1. Which store has the maximum sales?
   - The total sales for each store are calculated using the `groupby()` function and sorted in descending order. The top 10 stores with the highest sales are selected and visualized using a bar plot.

2. Which store has the maximum standard deviation?
   - The standard deviation of weekly sales for each store is calculated using the `groupby()` function and sorted in descending order. The top 10 stores with the highest standard deviation are selected and visualized using a bar plot.

3. Identify holidays with higher sales than the mean sales during non-holiday weeks for all stores together.
   - Two subsets of data are created: one for non-holiday weeks and one for holiday weeks. The mean sales during non-holiday weeks is calculated, and the holidays with sales higher than this mean value are identified and displayed.

## Conclusion:
The project provides insights into the retail analysis of Walmart sales data. It highlights the stores with maximum sales, the stores with high variability in sales, and the holidays with higher sales compared to non-holiday weeks. Additionally, it presents visualizations of the monthly and semester sales trends and explores the relationships between weekly sales and other numeric features.
