**Video Games Sales Analysis**

This project is an archive of the analysis conducted on the Kaggle data set Video Games Sales. The data collection includes information on video game sales and ratings, as well as platforms, genres, publishers, and other characteristics.

**Description of the Problem**

The goal of this investigation is to learn more about video game sales and ratings. The analysis seeks to provide answers to problems such as:

- What are the most popular platforms?
- What are the most popular genres?
- Who are the most successful publishers in terms of sales?
- What is the distribution of game ratings?
- Is there a link between sales and ratings?

**Data Set Overview**

The data set contains 16,598 rows and 16 columns. The columns are:

- Rank
- Name
- Platform
- Year
- Genre
- Publisher
- NA_Sales
- EU_Sales
- JP_Sales
- Other_Sales
- Global_Sales
- Critic_Score
- Critic_Count
- User_Score
- User_Count
- Developer

The data set has missing values, duplicates, and inconsistent data types, which require cleaning and preprocessing before analysis.

**Directory Structure**

The directory structure for this project is as follows:
```
/videogamessales/
|-- data/
|   `-- data_documentation.md
|-- munge/
|   `-- data_transformations.md
|-- src/
|   `-- data_aggregations.md
|-- reports/
|   `-- Video Game Sales Data_Module 6.xlsx
`-- README.md
```
- The data folder contains the data_documentation.md file that documents the raw data set's attributes and instructions on how to retrieve it.
- The munge folder contains the data_transformations.md file, which documents the transformations applied to the data set.
- The src folder contains the data_aggregations.md file, which documents the aggregations applied to the data set.
- The reports folder contains the video_games_sales.xlsx file, which includes the visualizations created in the module 6 assignment. The visualizations are also saved in the visualizations folder within the reports folder.
- The README.md file contains a description of the problem analyzed and the insights found.

**Data Preprocessing**

Preprocessing is required to resolve missing values, duplicates, and mismatched data types in the data collection. Preprocessing stages include:

- Removing columns that are irrelevant to the analysis.
- Managing missing data by removing rows or filling them with relevant values.
- Managing duplicates by removing or maintaining them based on the context.
- Transforming data types to the proper format.

**Data Aggregation**

All sales for each platform, genre, and publisher are included in the aggregated data set. The following aggregations were performed:

- Sorting the data set by platform, genre, and publisher.
- Determining the total sales for each category.

**Key Findings**

The examination of the Video Game Sales data set yielded numerous insights:

- The PlayStation 2 is the most popular platform, followed by the Xbox 360 and PlayStation 3.
- The most popular genre is Action, followed by Sports and Shooter.
- Electronic Arts, Activision, and Nintendo are the top three game publishers in terms of sales.
- The majority of the games in the data set have ratings ranging from 4 to 8.
- There is a positive relationship between sales and ratings.
