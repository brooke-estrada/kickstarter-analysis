# Kickstarting Kickstarter Analysis

## Overview of the Kickstarter Project

### Purpose

In this week's challenge, we helped Louise make decisions on her upcoming play "Fever". Louise's play "Fever" almost met its funding goal, and she hypothesized that the campaign's success is affected by its launch date. We analyzed data from a "crowdfunding" campaign website to gather insights on what specific factors affect a campaign's success. In reviewing the data, we analyzed two factors: launch dates and the percentage of success base on if their funding goal was met. We then further observed these trends by creating visualizations of the campaign outcomes. Our hope was to provide Louise with helpful insights so that she makes informed decisions about her play's budget and release date in order to have a successful campaign.

In helping Louise, we learned to import data to a table for analysis, apply filters, generate/interpret pivot tables, and calculate the measures of central tendency: mean, median, mode, standard deviation, and variance in Excel. We also learned to identify outliers in the data set and create/interpret data visualizations.

### Analysis and Challenges

#### Deliverable 1: Analysis of Outcomes Based on Launch Date

Our first analysis was to visualize campaign outcomes based on their launch date. We created a Pivot table and used the filter icon to display “Parent Category” and “Years.” To do so, we created a new column and extracted the year from the “Date Created Conversion” by using the YEAR() function. See below for an example.

=YEAR(S2) Where S2 was the "Date Create Conversation" column.

We placed “Parent Category” and “Years” in the filter field of the pivot table wizard tool. We then placed the “Outcomes” in the column and value fields and “Date Created Conversion” in the rows field. To further analyze the outcomes of the campaigns, we filtered the pivot table to display only theater campaigns, and show “successful,” “failed,” and “canceled” for the column labels. We then filtered them in Descending order. Finally, we created a chart to visualize the three types of outcomes (successful, failed, and canceled) over time. Below is the graph and screenshot of the excel sheet.

![](https://i.imgur.com/ruUGHjn.png)

![](https://i.imgur.com/51LgMZP.png)


#### Deliverable 2: Analysis of Outcomes Based on Goals

For our second analysis, we created a visualization to look at the percentage of "successful," "failed," and "canceled" plays based on the funding goal amount. We used the `COUNTIF` function to produce the number of successful, failed, and canceled plays based on their goal range. We then calculated the total projects per goal range and the percentage of "success," "failed," and "canceled" per goal range. After calculating the percentage of outcomes per goal range, we created a line graph to observe the three outcomes based on their goal ranges. Below is the line graph and screenshot of the excel sheet.

![](https://i.imgur.com/g2ASw0z.png)

![](https://i.imgur.com/qOSCwJ7.png)


### Challenges and Difficulties Encountered

In analyzing Louise’s data, there are a couple of aspects that were challenging to overcome. Initially, the data set combined the project category and sub-category in one column. This was an issue because Louise was particularly interested in knowing how projects classified as theater campaigns performed in hitting their goals and being successful.  We resolved this issue by splitting the column into two new columns: Parent Category and Parent Sub Category. We were able to accomplish this by using the the "Convert Text to Columns Wizard" tool to split the data into the two know columns. 

We also faced a challenge with the data set not including the average donation for each campaign. This data point would be helpful for Louise to visualize the outcomes of the theater campaigns. To do so, we created a new column for the Average donation by dividing the pledged amount by the number of backers. We nested this equation in a `ROUND()` function, which rounded the average donation to a whole number. This equation provided the average amount each backer pledged per campaign. However, we ran into our third challenge with a `#DIV/0!` error. This was because not all campaigns had a backer, and those campaigns were given a zero. This error occurred because numbers are not divisible by zero. We corrected this error by using the `IFERROR()` where we could replace the error with a user-defined input, in this case, we defined it as “0.”

### Results and Conclusions

#### Outcomes Based on Launch Date
1. Theater campaigns were most successful during the summer months: May, June, July, and August. There was another increase and peak of successful campaigns in February, and October.
2. However, we did see an increase in failed campaigns during the same months, but they did not overcome the successful campaigns. We also saw an overal drop in successful and failed campaigns during the winter months: November, December, and January.


#### Outcomes Based on Goals
100% of the plays that had a funding goal between $45,000 and $49,999, failed. The most successful play campaigns had a funding goal of less than $1000 with 75% of the plays were able to meet their funding goal. Similarly occured for campaigns with a funding goal between $35,000 and $45,000. 


### Limitations

In this data, we were limited to analyzing theater campaigns because Louise already had a play in mind to launch. In this data set, plays were a sub-category of the parent category "theater." The category encompass all types of plays except musicals (which were defined separately). This could be a potential limitation as some plays could be more or less successful (i.e. when comparing comedies to tragedie). We also did not compare campaign outcomes to other factors such as Percentage funded, Spotlight, or the number of backers per play. 

We also analyzed campaigns laterally via time. To further explore the idea of successful campaigns, we didn't look into other stagnant factors like the Percentage Funded or if they used a spotlight campaign. These aspects may have provided further insights on successful campaigns prior to the launch date. They could also pre-determine the success of a campaign prior to a launch date being picked.

### Future Analysis
To further explore the success of theater campaigns, we could conduct a correlation analysis to determine if successful campaigns were related to their launch dates. It would also be helpful to consider the marketing campaigns or the spotlight feature in affecting the campaign outcomes. A more in-depth look at play genres could also be insightful in determining factors that affect the campaign outcomes.
