You must perform simple transformations on your data (you might need to reload the data in HDInsight and Hive).  

Do the following steps:
1. Create a new table for your analysis call “sales_genre”.  
   - Load the table “sales” into this table.
   - Select these columns: Genre, Global_Sales, Critic_Score.   
2. Round the data found in the “Global_Sales” column.  (HINT:  the SQL function to round a number is ROUND(obs)
3. Filter the data to only look at those items in the “Critic_Score” column that are greater than 0.
4. Order the data in the “Critic_Score” column from highest to lowest. (HINT:  Use the DESC query)


```
DROP TABLE sales_genre;
CREATE EXTERNAL TABLE sales_genre

(
  Name string,
  Platform string,
  Year_of_Release int,
  Genre string,
  Publisher string,
  NA_Sales float,
  EU_Sales float,
  JP_Sales float,
  Other_sales float,
  Global_sales float,
  Critic_Score int,
  Critic_Count int,
  User_Score float,
  User_Count float,
  Developer string,
  Rating string
)

ROW FORMAT DELIMITED FIELDS TERMINATED BY ','
LINES TERMINATED BY '\n'
STORED AS TEXTFILE LOCATION '/sales'
TBLPROPERTIES("skip.header.line.count"="1");
```

Screenshots for reference:

