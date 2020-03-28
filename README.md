# Project 1: SAT & ACT Analysis

By Luken Weaver, GA Data Science Immersive, 2020



## Problem Statement

Identifying key factors influencing participation and rates and scores in various states using aggregate SAT and ACT


## Executive Summary

The aim of this project is to present findings of our data analysis to the College Board, with the goal of recommending data-informed conclusions regarding how to raise SAT participation rates in states across the country, using provided state data sets and some supplementary research.

Provided four data sets in cvs format, we were tasked to evaluate the provided data, fix discrepancies and missing entries, adjust data types, and reconcile all data such that it could be merged into one accurate and comprehensive dataframe for use in our exploratory data analysis.

After some preliminary EDA, we then processed that information into useful data visualizations.

At each step, we identified patterns and outliers, which drove further, more focused, data analysis and visualization.

Ultimately, we presented a summary of our findings in a PowerPoint presentation.


####  Data Dictionary 

Feature titles are patterned *tyy_sub* where *t* is test, *yy* is year, and *sub* is the shortened subject name.  A quick guide is included first for ease of use, followed by a full dictionary.

Quick Guide:

|Title Element|Element Type|Description|
|---|---|---|
|a|t|ACT|
|s|t|SAT|
|17|yy|2017|
|18|yy|2018|
|par|sub|Participation|
|mat|sub|Math|
|eng|sub|English|
|rea|sub|Reading|
|sci|sub|Science|
|com|sub|Composite|
|ver|sub|Evidence-Based Reading and Writing (verbal)|
|tot|sub|Total|

Full Data Dictionary:

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|All| The state for which the data applies|
|a17_par|float|ACT 2017| Participation rate, 2017|
|a17_eng|float|ACT 2017| Mean English score, 2017|
|a17_mat|float|ACT 2017| Mean Math score, 2017|
|a17_rea|float|ACT 2017| Mean Reading score, 2017|
|a17_sci|float|ACT 2017| Mean Science score, 2017|
|a17_com|float|ACT 2017| Mean Composite score, 2017|
|s17_par|float|SAT 2017| Participation rate, 2017|
|s17_ver|int|SAT2017| Mean Evidence-Based Reading and Writing score, 2017|
|s17_mat|int|SAT2017| Mean Math score, 2017|
|s17_tot|int|SAT2017| Mean Total score, 2017|
|a17_par|float|ACT 2018| Participation rate, 2018|
|a18_eng|float|ACT 2018| Mean English score, 2018|
|a18_mat|float|ACT 2018| Mean Math score, 2018|
|a18_rea|float|ACT 2018| Mean Reading score, 2018|
|a18_sci|float|ACT 2018| Mean Science score, 2018|
|a18_com|float|ACT 2018| Mean Composite score, 2018|
|s18_par|float|SAT 2018| Participation rate, 2018|
|s18_ver|int|SAT2018| Mean Evidence-Based Reading and Writing score, 2018|
|s18_mat|int|SAT2018| Mean Math score, 2018|
|s18_tot|int|SAT2018| Mean Total score, 2018|

## Conclusions and Recommendations

 
The basic trends are inertia, bimodality, sampling bias, and zero sum status.
    
States tended to stay with one test, and perform similarly year to year.  Big changes in participation were rare and due to discrete and identifiable interventions at the state level.
    
Participation rates tended toward two distinct clusters: a set of high participation states that either mandated a particular test or proctored it at state expense, and another set of states that participated at middling rates voluntarily or as a supplement to the other test.
    
As participation increases, score returns decrease.  This is likely due to the supplementary status of the less-taken test selecting for motivated students who are confident that they test well enough that taking the second test will help their college chances.  Mandatory testing includes students who do not plan to continue their education after high school and will be less motivated to prepare.
    
States do not mandate both tests.  At most, they will mandate one or the other, and it is likely that even if they are not mandatory, the familiarity of being more common in an area will lead to that being the 'default choice' for students who do wish to take a test, but not necessarily both.  There 'gravity' effect that pulls participation rates toward low or high extremes as a test gets more or less common.
    
Colorado and Illinois were flipped by the SAT winning state contracts to become the state's mandatory test, proctored at state expense.  One cited reason for this was that the SAT revamped the test in 2016 to be more in line with Common Core standards, making the SAT freshly relevant as a valid assessment tool for school systems rather than a general test of student aptitude.  State contracts are the biggest targets, and by considering state needs such as assessment, the design and marketing of the SAT can be made more appealing.
    
The other approach is to look at states that have no true center of gravity, ACT or SAT, yet, and might be considered up for grabs.  A state like Florida that is considering instituting mandatory testing, but not yet one in particular, could be won 'piece by piece' until it makes sense just to make that the official test (it should be noted that the same bodies open to mandatory testing in Florida also voice some displeasure with the Common Core, so a different marketing approach would be warranted in these areas).  The SAT lost market share to the ACT between 2017 and 2018, and while Florida may continue to buck the 'one or the other' trend, it seems likely that over time, if participation rates are not increased, they will decrease in favor of the competition.