# Home_Sales
Module 22 UM Bootcamp Challenge

## Background
For this challenge, I used SparkSQL to determine key metrics about home sales data. Then used Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.  I did this using Google Collab.

## Steps
1. First the dependencies were imported and installed.  The files were read into Google Collab via the url = "https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv"
2. The temporary view HomeSales was created.

## Results
1. What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.<br>
+----+-------------+<br>
|year|average_price|<br>
+----+-------------+<br>
|2019|     300263.7|<br>
|2020|    298353.78|<br>
|2021|    301819.44|<br>
|2022|    296363.88|<br>
+----+-------------+<br>

2. What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.<br>
+----------+-------------+<br>
|year_built|average_price|<br>
+----------+-------------+<br>
|      2010|    292859.62|<br>
|      2011|    291117.47|<br>
|      2012|    293683.19|<br>
|      2013|    295962.27|<br>
|      2014|    290852.27|<br>
|      2015|     288770.3|<br>
|      2016|    290555.07|<br>
|      2017|    292676.79|<br>
+----------+-------------+<br>

3. What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.<br>
+----------+-------------+<br>
|year_built|average_price|<br>
+----------+-------------+<br>
|      2010|    285010.22|<br>
|      2011|    276553.81|<br>
|      2012|    307539.97|<br>
|      2013|    303676.79|<br>
|      2014|    298264.72|<br>
|      2015|    297609.97|<br>
|      2016|     293965.1|<br>
|      2017|    280317.58|<br>
+----------+-------------+<br>

4. What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.<br>
(top 5 showing)
+----+-------------+<br>
|view|average_price|<br>
+----+-------------+<br>
|  51|    788128.21|<br>
|  52|    733780.26|<br>
|  53|     755214.8|<br>
|  54|    798684.82|<br>
|  55|    771153.32|<br>

This query ran in --- 1.1464893817901611 seconds ---

5. The temporary table was cached.
6. Running the query again resulted in it running in --- 2.865172863006592 seconds ---
7. The table was partitioned and ran through parque then ran again in only --- 1.085845708847046 seconds ---
   The partitioned table ran much faster than when the table was just cached.
9. The table was uncached.

## Credits
Thank you to Hunter Hollis, instructor, and TA's Randy and Sam for this week's instruction. Also, thank you to tutor, Limei Hou, who reviewed my code and helped me re-format to measure the correct run times.
