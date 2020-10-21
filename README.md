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
    There are 53 columns totally. 3 of them were completely blank so we dropped them completely.
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
