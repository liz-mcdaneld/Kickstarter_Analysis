# Analysis of Kickstarter Campaigns

## Based on the trends in data, what is the best way to have a successful Kickstarter Campaign

### The purpose of this analysis is to see what correlations are present in successful Kickstarter Campaigns vs failed Kickstarter Campaigns. These outcomes will help decide the best route to take for starting a Theatre Kickstarter Campaign for upcoming plays.

## Analysis and Challenges
For this analysis I have filtered down our initial dataset to reveal trends and outcomes for the topic of Theatre Kickstarter Campaigns, specifically for plays. 
Using Excel, I applied filters to search for specific data based on region, goals, amount pledged, outcomes and much more. Through the Excel function [=Round(E2/D2*100,0), which is calculating the pledged amount divided by the goal amount, I created our percentage funded column. To find the average donation per backer on campaigns I created a column using the Excel function [=ROUND(E2/L2,2)], this is our pledged amount divided by our backer count. 
Using the “Text to Columns” function in Excel, with the “/” as our delimiter, I made two separate columns for Parent Category and Subcategory. This allows us to better filter and sort through which specific data we want to look at. 
To better understand our date created, date ended, and year of the Kickstarter, I converted the “deadline” and “launched at” columns to a more readable format using the function [=(((J2/60)/60)/24)+DATE(1970,1,1)]. This equation divides the data in the “launched at” column by sixty seconds, then by sixty minuets, and then by twenty-four hours. Then I used that result to tell Excel to apply the [DATE] formula by the Unix timestamp.
To further analyze the findings the Parent Category and Subcategory I have compiled statistics using a PivotTable and PivotChart in Excel. This lets us look directly at the count of outcomes for the Theatre Category.


### Analysis of Outcomes Based on Launch Date
Finding the subcategory statistics, I have changed the rows to be the subcategory data and added an additional filter of the “Parent Category” to the PivotTable and Pivot Chart.
Using the PivotTable and PivotChart in Excel allows us to look at the correlations between the outcomes of Kickstarter Campaigns and the Launch Date for all Kickstarter Campaigns.
By applying a filter for Parent Category, we can look at just the Theatre Outcomes by Launch Date. 
![](file:///c%3A/Users/lizly/OneDrive/Documents/Data%20class/Theater_Outcomes_vs_Launch.png.png)
If we look at the data for Theatre Outcomes by Launch Date, we can see that May and June had the highest amounts of launched campaigns during this time. We can also see that the success rate trends downward with the rest of the year. One of the months with the highest fail rate is December, with thirty-five failed campaigns out of a grand total of seventy-five launched. 

### Analysis of Outcomes Based on Goals
To find the relations of Kickstarter Campaign Goals and the Outcomes I have used the Excel function [=COUNTIFS]. This tells Excel to count the number of Successful, failed, and canceled outcomes using the Theatre Kickstarter Campaigns for Plays for our criteria. To find the percentage of the outcome counts, I applied the function in Excel [=ROUND] to divide outcome counts, by the Total project counts. The collection of this data is applied to a “Outcomes Based on Goal” line graph to visualize the data gathered. 
The data for Outcomes based on Goals revealed the goal range of less than $1,000, has a 76% success rate. While the goal range of $1,000 to $4,999 has a 73% success rate. We can see a trend in higher percentages of campaign failures as the goal increases past $19,999. 
![](file:///c%3A/Users/lizly/OneDrive/Documents/Data%20class/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
Challenges encountered with this analysis, is working with a large source of data, and narrowing it down to exactly what is desired. Without the use of filters this would be a lengthy process to do. Other challenges that could have happened is having a shorter time span of data collection, shorter sets of data make trends harder to pinpoint. 



## Results

###Conclusions found about the outcomes based on launch date. 
Reviewing the Outcomes Based on Launch Date trends, the month of May and June had the highest success rate of launch, the lowest success rate is August through December. We can conclude that the best time to launch a new campaign would be either May or June, and the worst time to launch would be after June, specifically December.

###Conclusions for Outcomes based on Goals
The more that a goal is decreased below the range of $10,000 to $14,999 the percentage rate of success increases. Focusing on the funding goal range of $10,000 to $14,999, we have a failed percentage rate of 46% and success rate of 54%. The graph “Outcomes Based on Goals” allows us to visualize trends of successful outcomes vs failed based on funding goals. 

###Limitations of this dataset
The limitation of this dataset is that we do not get a look into how the Goal of the Kickstarter Campaigns is delegated towards the project. Being able to see what percentage of the Goal goes towards certain aspects of the project allows the consideration of what budget cuts are possible to make a lower asking price of a Kickstarter. By knowing this information and making budget cuts where possible, a person could ask for a lower range on the goal. These lower priced goals have shown to be part of the more successful Kickstarter Campaigns. 

###Possible Further Analysis
Other graphs and data that we could create to pinpoint the best outcome for the purpose of this analysis is finding the genre of the theatre plays and how that could affect the outcomes of the Kickstarter Campaigns. There could also be additional PivotTables, and Pivot Charts created to see if there is any connection with a successful campaign being a “staff pick” or “spotlighted.”
