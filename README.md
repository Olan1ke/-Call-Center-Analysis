![image](https://github.com/Olan1ke/-Call-Center-Analysis/assets/127860303/c9803964-295d-4dac-9083-aad9797db818)# Call Center Analysis

## Introduction
This data is about a call center,we were asked to give insight about the customer and call agent behaviour,

## PowerBi Concept Applied;
1. PowerBi Query Editor
2. DAX
   
## Problem Statement
•	Overall customer satisfaction
•	Overall calls answered/abandoned
•	Customer Satisfaction Rating per Time
•	Average speed of answer
•	Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

## Data Sourcing
This data from PWC Forage Internship. The dataset is in Excel workbook format, encompassing one table, The table has 10 columns and 50000 rows,The column header are;Call Id,Agent,Date,Time,Topic,Answered (Y/N),Resolved,Speed of answer in seconds,AvgTalkDuration,Satisfaction rating

## Data Cleaning/Transformation
I used power query editor in PowerBi for the cleaning and transformation, These are the steps taken;
1. change some data type
2. Some of the time had the date/time data type
3. I change it to time alone
4. I change the Y/N in call Answered and Resolved column Yes/No
I use DAX to create the following measures;
1.  CallLengthSeconds = 
    TIMEVALUE([AvgTalkDuration]) * 3600 + 
    MINUTE([AvgTalkDuration]) * 60 + 
    SECOND([AvgTalkDuration])
2. I created a new measure,OverallSatisfaction = AVERAGE(Call_Center[Satisfaction rating])

## Data Analysis And Visualization
## Conclusion And Recommendation
