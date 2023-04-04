The raw data set for the Video Games Sales dataset can be found on Kaggle at: https://www.kaggle.com/rush4ratio/video-game-sales-with-ratings. You will need to sign up for a free Kaggle account to download the data set.

Once you are signed in to Kaggle, click on the "Download" button on the dataset page to download the "Video_Games_Sales_as_at_22_Dec_2016.csv" file.

Save the downloaded file to your local machine.

Next step, you will load your business problem data into HIVE.
1)	Load your csv file in HDInsight using the Azure Storage Tool.  Put the data in a container called Sales
2)	Create a schema and load the data from Azure Storage into Hive.  Call the table, “sales”.
```
DROP TABLE sales;
CREATE EXTERNAL TABLE sales

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

3)	Validate that the schema is correct using the “table view” tab.
```
SELECT * FROM sales;
```
4)	Inspect the data were loaded properly using the SQL query interface
