## Overview
The 'Dashboard' offers charts that change in real-time with changes in records. The main aspect of the dashboard is to make your data 'prettier' and presentable. The charts are portrayed in different formats like pie charts, line charts, bar charts.  

## Basic Insight
The charts in the dashboard are pulled from an internal sheet that keeps the data in PivotTables. Every table in the 'Analysis' Worksheet has a (table) name which will be referred to, within single quotes (' '), in this file. 

## Getting Started
To use the template properly, I'd advise you to CREATE A NEW SHEET (let's call it "GoalSheet") for storing the following data:
- Goal Scorer
- Goal Assister
- Competition/League
- Mode of Goal
- Mode of Assist
- Goal Placement (Inside/Outside)  
- Goal Timings

Order can be altered. With this set-up, you are now ready to remove all errors in the 'Analysis' Worksheet and a step closer to portraying your data in those beautiful charts.

Under the empty fields of 'GoalsTable', 'AssistsTable', 'Competitions' in the 'Analysis' worksheet, you have put the names of your scorer/assister/competitions. The fastest way to do it is to copy/paste all the scorer/assister from your 'GoalSheet' with all the duplicates removed.
```
Data (TAB) > Delete Duplicates
```
You can use the pre-existing assists-modes and goal-modes or use your own.
### The #REF! Error
> #REF error (the “ref” stands for reference) is the message displayed when a formula references a cell that doesn't exist.

Since you have your 'GoalSheet' set up, now you have to refer your (error-ed) cells to appropriate columns to get the desired result. For example: In the 'Competitions' Table, the code will be:
```
=COUNTIF(GoalSheet!$D$3:$D$100,$N15)
```
..where '$N15' is the name of the competition you entered in the 'Analysis' Worksheet and 'GoalSheet!$D$3:$D$100' refers to the column your 'GoalSheet' Worksheet where you are storing the data for 'Competition/League'

### Resources
Background Image by **Abigail Keenan** on *Unsplash*.