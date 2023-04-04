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

Screenshots for reference:

![1 - Create Table](https://user-images.githubusercontent.com/128261514/229655864-443ebea0-3a61-4aea-9ad9-f9cea5bc94ad.png)
![2 - TABLE - Columns 1](https://user-images.githubusercontent.com/128261514/229655866-0f43dd8d-176f-4bbb-9da8-05362350aaa7.png)
![2 - TABLE - Columns 2](https://user-images.githubusercontent.com/128261514/229655867-e41bb503-b8a8-4bd3-a57c-dda90f639195.png)
![3 - Inspect  Query 1](https://user-images.githubusercontent.com/128261514/229655868-3d04791f-d833-4096-999a-3c1880b87130.png)
![3 - Inspect  Query 2](https://user-images.githubusercontent.com/128261514/229655870-5438c34d-13f1-42b4-af5e-e66cb7c917e4.png)
![TABLE - DDL 1](https://user-images.githubusercontent.com/128261514/229655872-2e804317-d030-40ba-93d8-2408631d141f.png)
![TABLE - DDL 2](https://user-images.githubusercontent.com/128261514/229655874-bccdd2ce-6972-40cb-a4ac-ab451ff36b5c.png)
![TABLE - Statistics](https://user-images.githubusercontent.com/128261514/229655875-db273bf8-5b84-48cc-bb29-d07c37bf2267.png)
