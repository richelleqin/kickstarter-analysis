# Kickstarting_Analysis
## Overview of Project
### Purpose
Kickstarter is a global crowdfunding platform that enables creators to acquire the monetary needs required to launch their creations. The way the funding goals are successfully reached is based on many factors. The purpose of this analysis is to help Louise launch more successful future campaigns by determining the relationship between the campaign outcomes to the launch date, and the campaign outcomes to the goals amount. 
## Analysis and Challenges
### Analysis of Outcomes Based on Launch Date
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/67567087/147794923-a62d38bb-361b-4790-97f8-97a8e512a066.png)

Based on the attached graph, the ratio of successful campaigns to failed campaigns seems to rise significantly during May and June, suggesting these campaigns fare better overall compared to other months. Although there is an increase in new campaign launches in summer (May to August) and October, the ratio of success to failure is overall much better in May and June (around 2 successes per failure), compared to July, August, or October. Further, it is clear that as the launch date gets closer to December, the success to failure ratio decreases. This makes sense as funds are needed for families towards the end of the year as compared to the summer. 
### Analysis of Outcomes Based on Goals
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/67567087/148289445-a7730669-3975-4886-844e-d00673a9b9f4.png)

Based on the graph, the highest success rate of 76% occurs for a goal that is less than 1000, and it decreases to a point of 20% success rate for a goal of 25,000 to 29,999. If we were to ignore the rebound at 35,000 to 44,999, then we can suggest that there is a negative correlation between goal amount and success rate. This makes sense as a high goal is harder to reach and more prone to failure. The rebound could be due to many factors (different campaign rewards, currency factors such as strength of dollar, or timing and seasonality), and as there is not sufficient data to support the notion that the rebound will always occur during those goal amounts, we can safely ignore it. 
### Challenges and Difficulties Encountered
The challenge that occurred during this analysis was on the goal amount and pledge amount currency. As there isn’t a clear indication for what currency this amount is converted to, we can only assume that all amounts listed is under the USD currency and not the currency shown in its respective columns. Further if this is not true, the conversion of currency is dependent on time, and we would have to join this to a time-based currency exchange rate table for accurate conversions. This could skew the data for the goals vs success rate analysis if the currency was not all USD. 
## Results
### Conclusions
In terms of launch date, it is concluded that the best time to launch campaigns for the highest success occurs during May and June. Further, campaigns should not be launched as we get nearer to December, as people will spend more money shopping for the holidays limiting their budget for crowdfunding. 
More campaigns tend to be launched during May, June, July, August, and October, and seasonality does not impact cancelled campaigns. 
 
In terms of goals, it is concluded that there is a negative correlation between goal amount and success rate. As the amount increases, it is harder for a campaign to achieve successful funding. 
### Limitations
There are some limitations on this dataset:
1) This dataset contains multiple currencies but have no indication of the currency currently set on the amounts. To account for a correct currency conversion, we must have the exchange rate from the time in which the campaign launched and when the person pledges. This may cause accuracy issues and campaigns that are successful on paper may not be successful during completion when funds are transferred. 
This exchange rate could also account for the strength of the dollar at the time, furthering the analysis to the motivation behind funding ($1 in 2009 is worth more than $1 in 2017). 
3) Live campaigns are currently ignored as they have not yet reach completion. However there are live campaigns that are successful already (i.e. pledge>goal) or close to failure already (i.e. pledge is much less than goal with limited time left), and these should be accounted for in our analysis. Further this means that the analysis is not considering the most recent data.
4) Further to 1, we are currently not looking into different years. Instead, we group every campaign into each month. This causes an issue with seasonality as kickstarter was launched in 2009. This means that there is a tendency that we have less campaigns in the early years, and more campaigns in the later years as the community grows. Further, as there were less competitions in the beginning and more chances for “clicks”, there was a much higher success rate compared to more recent data. To better our analysis, it is best to analysis more recent campaigns outcomes than the earlier campaigns. 
### Possible Graphs/Tables
Some possible graphs for future analysis: 
1) A bar graph of the successful rate of parent categories
    - We could be more proactive by figuring out those parent categories that are less likely to be successful. Thus, we can plan/target ahead before launching a specific category. 
![Picture2](https://user-images.githubusercontent.com/67567087/147795037-26435c72-627c-450d-b741-c25ddd043614.png)

2) A graph of campaign duration vs outcome. 
    - This allows us to determine if a longer campaign period amount to higher success rate.
![Picture1](https://user-images.githubusercontent.com/67567087/147795046-535db260-8c43-4a3a-a67b-e8eea9c505cd.png)

3) A campaign reward table could be possibly added to join with Kickstarter table in our analysis.
    - A higher reward campaign could attract more people to contribute that may lead to a higher success rate.
