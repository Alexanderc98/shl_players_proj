# Exploratory analysis of hockey players in the SHL

* Performed exploratory analysis to help hockey teams understand their data better.
* Scraped 448 hockey players from shl.se using python and beautifulsoup.
* Performed hypothesis testing to see if the differences, found in the data, between being a forward or defender is statistically significant.
* Used Bonferroni correction since I was testing multiple hypotheses.
* Built a linear regression model to quantify the correlation between hits and penalty minutes.

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
* Split player name variable into first name, last name and full name
* Transformed Time on Ice / Games Played (mm:ss) to show everything in seconds instead

## EDA
Below are a few highlights of my exploratory analysis.

![alt text](https://github.com/Alexanderc98/shl_players_proj/blob/main/pictures/player_penalty_minutes_split_by_teams.PNG "player_penalty_minutes_split_by_teams")


![alt text](https://github.com/Alexanderc98/shl_players_proj/blob/main/pictures/correlation_between_hits_and_penalty_minutes.PNG "correlation_between_hits_and_penalty_minutes")


![alt text](https://github.com/Alexanderc98/shl_players_proj/blob/main/pictures/assists_in_a_season_split_by_position.PNG "assists_in_a_season_split_by_position")



### Top 5 players with most penalty minutes in shl regular season 2021/2022

![alt text](https://github.com/Alexanderc98/shl_players_proj/blob/main/pictures/top_5_penalty_minutes.PNG "top_5_penalty_minutes")
