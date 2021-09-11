# Basic analysis of NBA season stats
This dataset explores the stats of basketball players
Dataset used: https://www.kaggle.com/drgilermo/nba-players-stats
Date: November, 2019

No of Columns:53

No of Rows:24691

No of numerical columns:47

No of categorical columns:6

NAN values: Present

# Part 1: Data Cleaning:
    There are 53 columns totally. 3 of them were blank so we dropped them completely.
    In the remaining 50 columns, NaN values were present. For those numerical problems, we replaced 
    all NaN values in numerical columns with the average of each column. The rows, where the missing values 
    were Player name, Team Name and position, were dropped.
    
    Rows remaining after cleaning : 24624 ( 67 rows removed, as player name, team and Position were missing for them)
    Columns after cleaning: 50 (3 columns with no values were dropped)

# Part 2: Normalization and Standardization:
    To normalize variables, we calculated the maximum and minimum value in each numerical column and 
    used the formula x~i=(xi−xmin)/(xmax−xmin) on every cell, to get values between 0-1.
    For most of the calculations, the data was standardized (by subtracting the mean from each value
    in a column and dividing it by its standard deviation), rather than normalized, to give both negative
    and positive values, with mean as 0 and standard deviation as 1.
![image](https://user-images.githubusercontent.com/57229722/132940806-04e54e39-5b8e-45d6-a1a5-eb9a638a99a6.png)

# Part 3: Data Visualization:
    We decided to compare the teams which perform more number of fouls and less number of fouls and see if the same 
    teams perform differently when it comes to total number of points.
![image](https://user-images.githubusercontent.com/57229722/132940860-f4d531c5-b603-4fbf-830b-4cf0cbd4c299.png)
    After calculating the total points for the teams with more fouls and less fouls we plotted a line chart to see if the 
    points and the fouls follow a pattern. We observed from the graph that the team with more fouls also have more points.
    The team Denver Nuggets, which has the most number of fouls has the second highest number of points and the team 
    San Diego Clippers, which had the lowest number of fouls had the poorest score when it came to points.
![image](https://user-images.githubusercontent.com/57229722/132940927-a7526f5a-ea86-4819-9de3-35c7da905616.png)
    Another interesting observation that we had made is the relation between the games started and total points for every
    player, and it was seen that the players with more points tend to start games.
![image](https://user-images.githubusercontent.com/57229722/132940944-02f821e3-6a6d-4e85-a644-cbe3773352f3.png)
# Part 4: Hypothesis Testing:
    # Hypothesis 1:
    We hypothesized that the mean age of the players playing for the team Boston Celtics was 26.98~27. 10 random players 
    taken as a sample were found to have their mean age as 29.1. We wanted to check if this observation was able to reject 
    our initial hypothesis, as there is a difference of 2 years between the two.

    H0: μ = 26.98

    H1: μ != 26.98

    α = 0.05
![image](https://user-images.githubusercontent.com/57229722/132941031-915d9a77-5a11-4ee5-9008-67e7eed43587.png)
    This means that the sample mean age of 29.1 is possible, and it does not reject the NULL hypothesis.
    We were able to use this because out of all the columns, age was one of the columns to have a Gaussian distribution
    
    # Hypothesis 2:
    We hypothesized that the mean no of blocks of the players whose age is 20 was 34.385. 10 random players with the same age 
    taken as a sample were found to have their mean no of blocks as 54.2. We wanted to check if this observation was able to reject 
    our initial hypothesis, as there is a difference of 19.815 in the no of blocks between the two means.

    H0: μ < 34.385

    H1: μ >= 34.385

    α = 0.05
![image](https://user-images.githubusercontent.com/57229722/132941088-98db3599-da5d-465a-815f-232079438162.png)
# Part 5: Correlation
    We will now find the Pearson's correlation coefficient for both the variables by taking 100 samples each, standardize it, 
    find its product, add it and then divide it by the number of observations. 
    The Pearson’s coefficient was found to be 0.777636.   
