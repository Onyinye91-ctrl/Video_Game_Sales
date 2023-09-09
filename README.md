### Video_Game_Sales

# Data Description
In this project i looked at video games sales using tableau and analyzed game data sales. The dataset contains a list of video games with sales greater than 100,000 copies. It has 16598 rows and 11 columns.

The columns/fields includes:

* Rank - Ranking of overall sales
* Name - The games name
* Platform - Platform of the games release (i.e. PC,PS4, etc.)
* Year - Year of the game's release
* Genre - Genre of the game
* Publisher - Publisher of the game
* NA_Sales - Sales in North America (in millions)
* EU_Sales - Sales in Europe (in millions)
* JP_Sales - Sales in Japan (in millions)
* Other_Sales - Sales in the rest of the world (in millions)
* Global_Sales - Total worldwide sales

For more information about the dataset visit [Kaggle](https://www.kaggle.com/datasets/gregorut/videogamesales). I used Tableau Public for my analysis and visualization.

# Data Transformation
I created three parameters Zone Sales, Start Date and End Date. Also, i care Game Date using the option create calculated field with the code `IF [Year] >= [Start Date] AND [Year] <= [End Date] THEN 1
ELSE 0 END` For Zone Sales i used the following code CASE [Zones Sales]
`WHEN "EU Sales" THEN [EU Sales]
WHEN "JP Sales" THEN [JP Sales]
WHEN "NA Sales" THEN [NA Sales]
WHEN "Other Sales" THEN [Other Sales]
WHEN "Global Sales" THEN [Global Sales]
END` Why do i have to create zone sales parameter while i can create my viz with each field? Reason is that i want to zones *(NA_Sales, EU_Sales, JP_Sales, Other_Sales and Global_Sales)* to be in one worksheet, creating many worksheet for each viz won't be ideal.


