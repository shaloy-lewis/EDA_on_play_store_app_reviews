<h1 align="center"> Exploratory Data Analysis on Play Store Apps</h1>
<h5 align="center"> AlmaBetter Verfied Project - <a href="https://www.almabetter.com/"> AlmaBetter School </a> </h5>

<p align="center"> 
<img src="images/googleplay.gif" alt="..." height="175px">
</p>

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 1. Abstract:
* Google play store is the official app store for all devices operating on the Android OS. It allows the users to browse and download the apps that are developed with the android software development kit (SDK).
* Apart from offering android applications and games, it also serves as a digital media store offering music, books, movies, and television programs.
* User ratings and reviews can significantly increase the number of app downloads; hence it is important to analyse the parameters which lead to users giving positive feedback and higher rating.
* Though this exploratory data analysis, we can understand and discover the key factors responsible for app engagement and success.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 2.	Introduction:
### We are provided with two datasets:
* Play_store_data: It contains the basic details of the app like number of user reviews, ratings, etc.
* User_reviews: It contains the user reviews and its sentiment score for the respective app.
We need to explore and analyze the data to discover key factors responsible for app engagement and success. 
### The contents of play_store_data are:
* App: It contains the name of the app with a short description (optional).
* Category: This section gives the category to which an app belongs. In this dataset, the apps are divided among 33 categories.
* Size: The disk space required to install the respective app.
* Rating: The average rating given by the users for the respective app. It can be in between 1 and 5.
* Reviews: The number of users that have dropped a review for the respective app.
* Installs: The approximate number of times the respective app was installed.
* Type: It states whether an app is free to use or paid.
* Price: It gives the price payable to install the app. For free type apps, the price is zero.
* Content rating: It states which age group is suitable to consume the content of the respective app.
* Genres: It gives the genre(s) to which the respective app belongs.
* Last updated: It gives the day in which the latest update for the respective app was released.
* Current Ver: It gives the current version of the respective app.
* Android Ver: It gives the android version of the respective app.

### The contents of user_reviews are:
* App: It contains the name of the app with a short description (optional).
* Translated_Review: It contains the English translation of the review dropped by the user of the app.
* Sentiment: It gives the attitude/emotion of the writer. It can be ‘Positive’, ‘Negative’, or ‘Neutral’.
* Sentiment_Polarity: It gives the polarity of the review. Its range is [-1,1], where 1 means ‘Positive statement’ and -1 means a ‘Negative statement’.
* Sentiment_Subjectivity: This value gives how close a reviewer’s opinion is to the opinion of the general public. Its range is [0,1]. Higher the subjectivity, closer is the reviewer’s opinion to the opinion of the general public, and lower subjectivity indicates the review is more of a factual information.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 3.	 Data pipeline:
* Once we have defined and understood the columns and the type of data it contains, it is necessary to eliminate the obvious errors, NaN values, and duplicates. Apart from this in some cases it is necessary to convert the datatype of the entries in the columns into more appropriate datatype.
* These were approached one column at a time. Following is a brief summary of how the error, NaN, and duplicate values were handled:
### a.	Play_store_data:
* Android Ver: The 3 rows containing NaN values were dropped from the dataset.
* Current Ver: The 8 rows containing NaN values were dropped from the dataset.
* Type: One row containing NaN value was replaced with a relevant entry.
* Rating: The 1470 NaN values were imputed with its median value.
* App: The duplicate values in the dataset were dropped.
* Apart from this the data present in different columns was manipulated to make them easier to analyse. Also, the datatype of the entries was changed in some cases to make the data relevant.
* The resultant number of rows post cleaning the data: 9649

### b.	User_review:
* All the rows containing NaN values were dropped.
* The resultant number of rows post cleaning the data: 37427

### c.	Data wrangling:
* Apart from this, two new columns were added to the main data frame, namely, “Rating Group”, and “Revenue”. This is done to improve simplify the analysis and come up with different meaningful visualizations.
Rating Group: This column groups the apps based on the average user rating. (4-5: Top rated, 3-4: Above average, 2-3: Average, 1-2: Below average).
*	Revenue: This column gives the revenue generated by the app through app installs alone.
By doing these operations on the original dataset, we are ready with the data pipeline, and data visualizations can be done on it.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 4.	Analysis Summary:
*	Percentage of free apps = ~92%
*	Percentage of apps with no age restrictions = ~82%
*	Most competitive category: Family
*	Category with the highest number of installs: Game
*	Category with the highest average app installs: Communication
*	Percentage of apps that are top rated = ~80%
*	There are 20 free apps that have been installed over a billion times
*	Minecraft is the only app in the paid category with over 10M installs. This app has also produced the most revenue only from the installation fee.
*	Category in which the paid apps have the highest average installation fee: Finance
*	Most popular app in the Play Store based on the number of reviews: Facebook
*	The median size of all apps in the play store is 12 MB.
*	The apps whose size varies with device has the highest number average app installs.
*	The apps whose size is greater than 90 MB has the highest number of average user reviews, i.e., they are more popular than the rest.
*	Helix Jump has the highest number of positive reviews and Angry Birds Classic has the highest number of negative reviews.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 5.	Challenges Faced:
*	Reading the dataset and comprehending the problem statement.
*	Examining the business KPIs for app development and devising a solution to the problem.
*	Handling the error, duplicate and NaN values in the dataset.
*	Designing multiple visualizations to summarize the information in the dataset and successfully communicate the results and trends to the reader.

![--](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 6.	Conclusion:
These are some of the aspects that the developer should research before proceeding with the app development. By conducting a simple exploratory data analysis (EDA) on the play store dataset, we not only eliminate avoidable risks of failure, but we may also be able to provide better ideas for building the app.

### From this EDA project, the following concepts were learnt:
*	Basic inspection of the raw data.
*	Examining the business KPIs for app development and devising a solution to the problem.
*	Handing the duplicate, error and NaN values present in the dataset, i.e., cleaning the data.
*	Using different Python functions and libraries to clean and manipulate data.
*	Data wrangling to come up with different insights on the data.
*	Designing multiple visualizations to summarize the information in the dataset and successfully communicate the results and trends to the reader.
