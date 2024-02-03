# SparkSQL/Big Data Challenge: Home Sales

This repository contains my work for the 22nd challenge of the UofT SCS edX Data Bootcamp.

Please note that `Home_Sales_colab.ipynb` contains the code written by me. `Home_Sales_starter_code.ipynb` contains the unaltered starter code provided by the bootcamp.

## Overview
In this challenge, you'll use your knowledge of SparkSQL to determine key metrics about home sales data. Then you'll use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Instructions

1. Rename the `Home_Sales_starter_code.ipynb` file as `Home_Sales.ipynb`

2. Import the necessary PySpark SQL functions for this assignment.

3. Read the `home_sales_revised.csv` data in the starter code into a Spark DataFrame.

4. Create a temporary table called `home_sales`.

5. Answer the following questions using SparkSQL:

    - What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

    - What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

    - What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

    - What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

6. Cache your temporary table `home_sales`.

7. Check if your temporary table is cached.

8. Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

9. Partition by the "date_built" field on the formatted parquet home sales data.

10. Create a temporary table for the parquet data.

11. Run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

12. Uncache the `home_sales` temporary table.

13. Verify that the `home_sales` temporary table is uncached using PySpark.

14. Download your `Home_Sales.ipynb` file and upload it into your "Home_Sales" GitHub repository.


## Summary
The average price of a four bedroom house sold in each year is:

\$300,263.70 in 2019 \
\$298,353.78 in 2020 \
\$301,819.44 in 2021 \
\$296,363.88 in 2022 

The average price of a three bedroom and three bathroom house built in each year is:

\$292,859.62 in 2010 \
\$291,117.47 in 2011 \
\$293,683.19 in 2012 \
\$295,962.27 in 2013 \
\$290,852.27 in 2014 \
\$288,770.30 in 2015 \
\$290,555.07 in 2016 \
\$292,676.79 in 2017 

The average price of a three bedroom, three bathroom, and 2 floor house built in each year is:

\$285,010.22 in 2010 \
\$276,553.81 in 2011 \
\$307,539.97 in 2012 \
\$303,676.79 in 2013 \
\$298,264.72 in 2014 \
\$297,609.97 in 2015 \
\$293,965.10 in 2016 \
\$280,317.58 in 2017 

Uncached vs Cached runtime comparison:

Uncached runtime: 0.70 seconds \
Cached runtime: 0.45 seconds
