# Excel Homework: Kickstart My Chart

## Background

Over $2 billion has been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the more than 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.

Getting funded on Kickstarter requires meeting or exceeding the project's initial goal, so many organizations spend months looking through past projects in an attempt to discover some trick for finding success. For this week's homework, I organized and analyzed a database of 4,000 past projects in order to uncover any hidden trends.

### Before I Began

1. Created a new space for this project called `excel-challenge` in either DropBox or Google Drive. **Do not add this homework to an existing space**.

2. Stored my excel workbooks in here and create a sharable link for submission.

## Instructions



Using the Excel table provided, I modified and analyzed the data of 4,000 past Kickstarter projects as I attempted to uncover some market trends.

* Used conditional formatting to fill each cell in the `state` column with a different color, depending on whether the associated campaign was successful, failed, or canceled, or is currently live.

  * Created a new column O called `Percent Funded` that uses a formula to uncover how much money a campaign made to reach its initial goal.

* Used conditional formatting to fill each cell in the `Percent Funded` column using a three-color scale. The scale should start at 0 and be a dark shade of red, transitioning to green at 100, and blue at 200.

  * Created a new column P called `Average Donation` that uses a formula to uncover how much each backer for the project paid on average.

  * Created two new columns, one called `Category` at Q and another called `Sub-Category` at R, which use formulas to split the `Category and Sub-Category` column into two parts.

  <img width="1011" alt="CategoryStats" src="https://user-images.githubusercontent.com/66078772/101654991-bbce3400-3a06-11eb-994c-697279830624.PNG">

  * Created a new sheet with a pivot table that analyzed my initial worksheet to count how many campaigns were successful, failed, canceled, or are currently live per **category**.

  * Created a stacked column pivot chart that can be filtered by country based on the table I created.

  <img width="807" alt="SubcategoryStats" src="https://user-images.githubusercontent.com/66078772/101655309-15cef980-3a07-11eb-98b6-6ca3b34dcfe6.PNG">

  * Created a new sheet with a pivot table that analyzed my initial sheet to count how many campaigns were successful, failed, or canceled, or are currently live per **sub-category**.

  * Created a stacked column pivot chart that can be filtered by country and parent-category based on the table I created.

* The dates stored within the `deadline` and `launched_at` columns use Unix timestamps. Fortunately, [there is a formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) that can be used to convert these timestamps to a normal date.

  * Created a new column named `Date Created Conversion` that will use [this formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) to convert the data contained within `launched_at` into Excel's date format.

  * Created a new column named `Date Ended Conversion` that will use [this formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) to convert the data contained within `deadline` into Excel's date format.

 <img width="973" alt="LaunchDateOutcomes" src="https://user-images.githubusercontent.com/66078772/101655675-79f1bd80-3a07-11eb-9c99-cb5475868ec9.PNG">

  * Created a new sheet with a pivot table with a column of `state`, rows of `Date Created Conversion`, values based on the count of `state`, and filters based on `parent category` and `Years`.

  * Then created a pivot chart line graph that visualizes this new table.

* Created a report in Microsoft Word and answered the following questions.

1. Given the provided data, what are three conclusions we can draw about Kickstarter campaigns?
*	The data provided shows that the Music and Theater campaigns have the highest successful rates with a 77 and 60 percent success rate.  Conversely, the Food and Games campaigns have the highest failure rate.  Overall, the data shows a 53 percent success rate and a 37 percent failure rate from all the Kickstarter Campaigns. 
*	The subcategory “Plays” was the most successful out of the “Theater” category due to the amount of successful campaigns within the total attempts in that subcategory.  However, the “Plays” subcategory also had the most total attempts out of all three subcategories.  For example, “Plays” had 1066 total attempts with 694 successful campaigns and the other two subcategories totaled 327 campaign attempts between the two campaigns. Comparatively, in the “Music” category, “Indie Rock” and “Rock” subcategories had the highest total attempts of campaigns and the highest percentage of success rate.   
*	Using yearly data for the most successful campaigns, besides a slight up tick in the months of May and June, campaign success rate appears to decline as the year progresses. 

2. What are some limitations of this dataset?
*	In the data set provided, there is not a column that tells you how much time is allotted to reach each campaign goal.  I see the start and stop dates of the campaigns but what I think be interesting is, was there a standard time length to meet your set goal.  If each campaign is judged with a different time scale, then the data set is not comparing apples to apples in that respect.  For example, if your goal were to raise 500 versus another campaigns goal was to raise 50,000 and you had 2 weeks to reach that goal, of course the goal of 500 is easier to reach in that time frame. 
*	I think the data should also digger deeper into location of the campaigns.  I think if you could compare data points such as demographics and economics of certain areas within the country it might give a better understanding why certain subcategories of theater and music campaigns were more successful than others, for example.  

3. What are some other possible tables and/or graphs that we could create?
*	I think that we could create a pivot table that shows average donation versus state results and then have a graph to maybe show a correlation between average donation versus results of campaign goals. 
*	Additionally, we could add the data that shows the time that it took the campaign to reach its initial goal based on Category to then plot to see if certain campaigns meet their goals quicker.  Even more, add in the demographics and economic data and plot together and show if there is a correlation with these factors. 


## Bonus

* Created a new sheet with 8 columns:

  * `Goal`
  * `Number Successful`
  * `Number Failed`
  * `Number Canceled`
  * `Total Projects`
  * `Percentage Successful`
  * `Percentage Failed`
  * `Percentage Canceled`

* In the `Goal` column, created 12 rows with the following headers:

  * Less than 1000
  * 1000 to 4999
  * 5000 to 9999
  * 10000 to 14999
  * 15000 to 19999
  * 20000 to 24999
  * 25000 to 29999
  * 30000 to 34999
  * 35000 to 39999
  * 40000 to 44999
  * 45000 to 49999
  * Greater than or equal to 50000

  ![GoalOutcomes](https://user-images.githubusercontent.com/66078772/101655908-c210e000-3a07-11eb-83b3-f3f19f657690.PNG)

* Used the `COUNTIFS()` formula, to count how many successful, failed, and canceled projects were created with goals within the ranges listed above. Populate the `Number Successful`, `Number Failed`, and `Number Canceled` columns with this data.

* Added up each of the values in the `Number Successful`, `Number Failed`, and `Number Canceled` columns to populate the `Total Projects` column. Then, used a mathematical formula, foound the percentage of projects that were successful, failed, or canceled per goal range.

* Created a line chart that graphs the relationship between a goal's amount and its chances at success, failure, or cancellation.

## Bonus Statistical Analysis

If one were to describe a successful crowdfunding campaign, most people would use the number of campaign backers as a metric of success. One of the most efficient ways that data scientists characterize a quantitative metric, such as the number of campaign backers, is by creating a summary statistics table.

Always up for the additional challenge, I evaluated the number of backers of successful and unsuccessful campaigns by creating **my own** summary statistics table.

* Created a new worksheet in my workbook, and created a column each for the number of backers of successful campaigns and unsuccessful campaigns.

  ![backers01](https://user-images.githubusercontent.com/66078772/101656366-3b103780-3a08-11eb-915f-d9fca1d00d55.png)

* Used Excel to evaluate the following for successful campaigns, and then for unsuccessful campaigns:

  * The mean number of backers.

  * The median number of backers.

  * The minimum number of backers.

  * The maximum number of backers.

  * The variance of the number of backers.

  * The standard deviation of the number of backers.

* Used my data to determine whether the mean or the median summarizes the data more meaningfully.
 *	I would say, for the successful data set, the median summarizes the data more meaningfully due to the huge difference from the lowest to the highest successful counts which are skewing the data.  For the failed data set it is not an issue since both results are so close in value. 

* Used my data to determine if there is more variability with successful or unsuccessful campaigns. Does this make sense? Why or why not?
 *	It appears that there is more variability with the successful campaign versus the failed campaigns.  Based on the data set this makes sense due to the fact that there is a huge difference from the mean versus the high of the data for the successful campaigns versus the failed campaigns. 


