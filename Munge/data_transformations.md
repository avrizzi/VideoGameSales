You must perform simple transformations on your data.  

Do the following steps:
1. Create a new table for your analysis call “sales_genre”.  


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

   ![1 a - create](https://user-images.githubusercontent.com/128261514/229656956-9d7385e0-cb0b-4e89-9c82-9edf664ac14b.png)

   - Load the table “sales” into this table.
   ![1 b - load](https://user-images.githubusercontent.com/128261514/229656965-c167746b-3123-4776-9d43-40449d211233.png)

   - Select these columns: Genre, Global_Sales, Critic_Score.  
   ![1 c - select](https://user-images.githubusercontent.com/128261514/229657029-e610c513-330f-4878-a996-304ce035b59a.png)

2. Round the data found in the “Global_Sales” column.  (HINT:  the SQL function to round a number is ROUND(obs)
   ![2 - round](https://user-images.githubusercontent.com/128261514/229657052-3cd012c8-af56-48dd-a1d6-c542789eed35.png)

4. Filter the data to only look at those items in the “Critic_Score” column that are greater than 0.
   ![3 - filter](https://user-images.githubusercontent.com/128261514/229657074-a7bd8f2f-5fe4-400c-a091-617da257b250.png)

6. Order the data in the “Critic_Score” column from highest to lowest. (HINT:  Use the DESC query)
   ![4 - order by](https://user-images.githubusercontent.com/128261514/229657084-ea12c1fc-dc8a-43c3-96bd-67b1453b2486.png)
