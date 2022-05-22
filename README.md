# Exploratory analysis of hockey players in the SHL

* Scraped 448 hockey players from shl.se using python and beautifulsoup.
* Performed hypothesis testing to see if the differences, found in the data, between being a forward or defender is statistically significant.
* Built a linear regression model to quantify the correlation between hits and penalty minutes.
* Used Bonferroni correction since i was testing multiple hypotheses.

## Code and Resources Used
**Python Version:** 3.79

**R Version:** 4.1.3

**Packages:** beautifulsoup, pandas, requests, dplyr, xtable, ggplot2, ggthemes, scales, cowplot, splitstackshape

## Web Scraping
I used beautifulsoup to scrape 448 hockey players from shl.se. With each player, we got the following:

* Jersey Number
* Player Name
* Position
* Games Played
* Goals
* Assists
* Total Points
* Penalty Minutes
* Game Winning Goals
* Power Play Goals
* Shots on Goal
* Hits
* Blocked Shots
* Plus Goal
* Minus Goal
* +/-
* Time on Ice / Games Played (mm:ss)
* Team

## Data Cleaning
After scraping the data, I made the following changes and created the following variables:

* Renamed columns so their name better reflect the content
* Transformed team and position to be a factor variable instead of a character variable
* Made a new column that shows if a player is still playing on the team or not, using a tell from the player name variable
* Split player name variable into first name, last name and full name.
* Transformed Time on Ice / Games Played (mm:ss) to show everything in seconds instead

## EDA

