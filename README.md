Video Games Sales Analysis

This project is an archive of the analysis performed on the Video Games Sales data set, which can be found on Kaggle here. The data set contains information on video games' sales and ratings, including platforms, genres, publishers, and other attributes.

Problem Description

The purpose of this analysis is to gain insights into video game sales and ratings. The analysis aims to answer questions such as:

- What are the best-selling platforms?
- Which genres are the most popular?
- Who are the top publishers in terms of sales?
- What is the distribution of ratings for games?
- Is there a correlation between sales and ratings?

Data Set Overview

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

Directory Structure

The directory structure for this project is as follows:

/videogamessales/
|-- data/
|   `-- data_documentation.md
|-- munge/
|   `-- data_transformations.md
|-- src/
|   `-- data_aggregations.md
|-- reports/
|   |-- video_games_sales.xlsx
|   `-- visualizations/
|       `-- visualization.png
`-- README.md

- The data folder contains the data_documentation.md file that documents the raw data set's attributes and instructions on how to retrieve it.
- The munge folder contains the data_transformations.md file, which documents the transformations applied to the data set.
- The src folder contains the data_aggregations.md file, which documents the aggregations applied to the data set.
- The reports folder contains the video_games_sales.xlsx file, which includes the visualizations created in the module 6 assignment. The visualizations are also saved in the visualizations folder within the reports folder.
- The README.md file contains a description of the problem analyzed and the insights found.

Data Preprocessing

The data set requires preprocessing to address missing values, duplicates, and inconsistent data types. The preprocessing steps include:

- Dropping columns that are not relevant to the analysis.
- Handling missing values by dropping rows or filling them with appropriate values.
- Handling duplicates by dropping or keeping them, depending on the context.
- Converting data types to the appropriate format.

Data Aggregations

The aggregated data set includes the total sales for each platform, genre, and publisher. The following aggregations were performed:

- Grouping the data set by platform, genre, and publisher.
- Calculating the sum of sales for each group.
- Calculating the mean and standard deviation of ratings for each group.

Key Findings

The analysis of the Video Games Sales data set revealed several insights:

- The best-selling platform is the PlayStation 2, followed by the Xbox 360 and PlayStation 3.
- The most popular genre is Action, followed by Sports and Shooter.
- The top three publishers in terms of sales are Electronic Arts, Activision, and Nintendo.
- The majority of games in the data set have ratings between 4 and 8.
- There is a positive correlation between sales and ratings.

Conclusion

This project archives the analysis of the Video Games Sales data set, which includes preprocessing, aggregations, and visualizations. The analysis provides insights into video game sales and ratings that can be useful for stakeholders in the video game industry.

Future analysts can use this archive to review and extend the analysis. They can replicate the preprocessing, aggregations, and visualizations to explore other research questions or to test different hypotheses.

Overall, this project demonstrates the importance of documenting and archiving data analysis to ensure reproducibility and transparency in research.