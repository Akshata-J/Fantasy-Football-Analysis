# Fantasy-Football-Analysis

Analysis of Fantasy Premier League

![FPL](https://user-images.githubusercontent.com/91014176/179262279-41246748-3a0e-4d19-a50a-6e6d83780d21.png)

image source : https://fanarena.com/wp-content/uploads/2019/11/Fantasy-Premier-League-Users-per-Season.png

### What is Fantasy Premier League?

FPL is a game that casts you in the role of a Fantasy manager of Premier League players. 

You must pick a squad of 15 players from the 2021/22 Premier League, who score points for your team based on their performances for their clubs in PL matches.

The following are the sequential steps needed for the analysis:
- Harvesting Data : 
  - Loading the data from the [Fantasy Premier League](https://fantasy.premierleague.com/) site for the year 2021-2022 till gameweek 35
  
  <img width="1121" alt="Screen Shot 2022-07-14 at 1 04 49 PM" src="https://user-images.githubusercontent.com/91014176/179042103-df88d63b-d515-4421-a49d-3500065a83ef.png">

- Exploratory Data Analysis : 
  -  top 10 players who have scored the maximum total points till the present gameweek
  <img width="1124" alt="Screen Shot 2022-07-14 at 1 05 04 PM" src="https://user-images.githubusercontent.com/91014176/179042158-b8c64173-368c-4000-9d42-c5699e767d88.png">

  -  teams getting most number of red cards and yellow cards
  <img width="1122" alt="Screen Shot 2022-07-14 at 1 05 39 PM" src="https://user-images.githubusercontent.com/91014176/179042225-e707c8cd-8753-4ca9-909f-681a24a40ebe.png">
  
  -  top 3 total points scorers of each teams
  <img width="1123" alt="Screen Shot 2022-07-14 at 1 06 43 PM" src="https://user-images.githubusercontent.com/91014176/179042370-f67c7a98-8004-42c9-a100-6441a0cacd38.png">
  
  -  players’ costs versus total points
  <img width="1118" alt="Screen Shot 2022-07-14 at 1 07 05 PM" src="https://user-images.githubusercontent.com/91014176/179042390-9639ea21-4fb7-4d50-83ba-d388395bc1c8.png">
 
## Problem Statement
The main purpose of this project to identify the following two things : 

1. Select the best possible combination of 15 player squad that is, formation of the best possible team to pick from the dataset 
- Formation of the best possible team to pick from the dataset
- With keeping in mind the budget and various player based constraints. Our aim is to maximize the points earned by this configuration
- The model is linear programming problem (LPP) where we have used the Linear Optimisation technique

<img width="895" alt="Screen Shot 2022-07-14 at 1 13 28 PM" src="https://user-images.githubusercontent.com/91014176/179043361-94b126c2-1321-48cf-a220-6f97c59a0324.png">

### Thoughts
- The dream team that was chosen is shown above
- We can see that the optimisation algorithm made sure that the constraints were followed. There are four defenders, four midfielders, and two forwards on the team
- It has also depleted the overall amount of money available to buy players, utilised 999
- And the highest possible total score is 2372

2. Make a prediction of how many points each player will score in the next game week 
- Predicting the points, a player will score in the upcoming gameweek : considering for 3 players - Hugo LLoris, Mohamed Salah, Heung Min Son
- Points each player will score in the next game week
- The Machine Learning algorithms used are Linear Regression model and Random Forest Regression

<img width="714" alt="Screen Shot 2022-07-14 at 1 22 08 PM" src="https://user-images.githubusercontent.com/91014176/179045116-a97aefad-4a90-4bb2-87cf-563eebc7d390.png">

<img width="713" alt="Screen Shot 2022-07-14 at 1 22 23 PM" src="https://user-images.githubusercontent.com/91014176/179045138-3461745c-9ec1-4cc3-9ddb-91a7eebcb755.png">

<img width="708" alt="Screen Shot 2022-07-14 at 1 22 42 PM" src="https://user-images.githubusercontent.com/91014176/179045159-3c402e9e-6b0a-41fa-aa19-10ca00891cbc.png">

- Linear Regression 

<img width="722" alt="Screen Shot 2022-07-14 at 1 23 25 PM" src="https://user-images.githubusercontent.com/91014176/179045181-b8e1302f-11aa-48ca-9c30-81e1bb0f6733.png">

<img width="721" alt="Screen Shot 2022-07-14 at 1 23 44 PM" src="https://user-images.githubusercontent.com/91014176/179045194-40ed2876-d04b-4759-a937-e13eca93c08c.png">

- Random Forest 

<img width="720" alt="Screen Shot 2022-07-14 at 1 23 59 PM" src="https://user-images.githubusercontent.com/91014176/179046591-7ff517f5-7ffe-4de4-b1ce-c371bba3871f.png">

<img width="719" alt="Screen Shot 2022-07-14 at 1 24 07 PM" src="https://user-images.githubusercontent.com/91014176/179046602-70930bda-e251-414c-9613-997722ea71bc.png">

### Thoughts
- We have predicted the total_points for the above mentioned players
- The most valuable player, on the other hand, will be the one with the greatest points and the lowest cost, i.e. the one with the highest points per cost (or points per million)

