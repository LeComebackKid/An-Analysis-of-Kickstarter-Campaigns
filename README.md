# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends
---
# Kickstarting with Excel

## Section 1:Overview of Project
###Purpose
The goal in this analysis is to evaluate if  Louise is likely to achieve success with her intended goal of crowdfunding $12,000 to fund her play, “Fever”. The results of this study will be used to help identify and evaluate factors that are complementary to a successful Kickstarter campaign. Using the data expressed in the Kickstarter Data Sheet, an analysis will be conducted by focussing on various elements and the way they have correlated in successful past campaigns. Some valuable and meaningful factors that will be considered relate to pledge goals, dates, location of the campaign, categories and subcategories

### Client Background
Louise is a playwright who is eager to launch her career in the world of theater. Her play, “Fever” - dark-comedy about her summer romance with Bill Murray - is already showing promise as a classic modern romance. All she needs is to bring these pages to life
In order to initiate this venture, she needs to organize her financing. Louise estimates that she will need to raise $12,000. She plans to obtain these funds using a crowdfunding campaign on Kickstarter. Louise is wondering if her goal could be actualized based on her estimates?

## Section 2: Analysis and Challenges

### About the Data
The Kickstarter dataset contains information from a wide variety of crowdfunding campaigns between 2011 and 2017. The data can be organized based on categories and location. There is also data available about pledge goals and donation totals, including the amount of backers. 

###Organization
There are two main foci that were analyzed compared to outcome - the date the campaign was launched and how the outcome fared in relation to the initial campaign goal.

Given the vast amount of information provided, a variety of filters and formats were set to help with organizing the data. Seeing as Louise is looking to raise money for a performance, the data was formatted to focus on the category of “theater” and, more specifically, the subcategory of “plays.” The designations, “successful”, “failed” and “canceled” also proved to be helpful in organizing the data and in creating visual representations of the data. 
The sheet was also organized to focus on financial goals and the amount pledged for each play. Using the formula =ROUND(En/Dn*100,0), an investigation was conducted to acknowledge the percentage of funds raised in relation to the set fundraising campaign goals. 

The data was also formatted to provide more insight about dates, by focusing on months and years. The provided data was delivered in a Unix Timestamp format, so the data had to be converted so that it could be properly interpreted. This was accomplished by using the formula =(((J2/60)/60)/24)+DATE(1970,1,1). With the dates converted, it was then possible to extract the specific year of each campaign. 
This data was then used to inspect the outcomes of theater campaigns based on the date they were launched. Using this information a pivot table (1.1 Theater Outcomes by Launch Date) was created showing the “successful”, “failed”, and “canceled” campaign counts per month. The table was formatted to focus on all campaigns which would fall under the category, “theater”. A line chart (1.2)  was additionally created to visualize this relationship between outcomes and launch month.
Table 1.1(path/to/filename.xlxs)
Graph1.1(path/to/filename.xlxs)
The focus then shifted to how the outcomes fared when compared to their campaign goals. This was accomplished by identifying how many campaigns would fall into one of three categories: A “successful” campaign, which met its goal; a “failed” campaign, which did not meet its goal; or a “canceled” campaign. 
The data was formatted to focus on the subcategory of “plays” and their outcomes. The data was broken down further to display the total number of campaigns based on their outcome brackets as seen in Graph 1.2, below. The information was then used to find the percentage results of each bracket. 
Graph1.2(path/to/filename.xlxs)
The data was accumulated using a COUNTIF formula to abstract the desired information from the larger data set. =COUNTIFS(Kickstarter!$D:$D,">=1000",Kickstarter!$D:$D,"<=4999",Kickstarter!$F:$F, "successful",Kickstarter!$R:$R, "plays"). The formula required looking at the pledged goals ($D:$D), the outcome qualifier ($F:$F, "successful",Kickstarter!$R:$R) that are plays ($R:$R, "plays") - all within the Kickstarter worksheet (Kickstarter!).

The data pulled into the chart to show the amount of “successful”, “failed” and “canceled” campaigns of plays. 
Table1.2(path/to/filename.xlxs)

###Challenges
There were a few challenges encountered during this analysis. For example, when creating the pivot table, Theater Outcomes by Launch Date (Table 1.1), there was the challenge of how to extract the months when focusing on the year. However, using the conversion dates, within the rows, allowed for this to occur. 

##Section 3: Results

###Conclusions Drawn About Theater Outcomes by Launch Date
- 1)Theater campaigns have proven to be mostly successful. 
The Theater Outcomes by Launch Date data demonstrates that it is likely the campaign will be successful. Every month contains data indicating a higher success rate when compared to campaigns that failed or were canceled. Overall, more than half were successful. However, when looking at the grand total before filtering the data to show only theater projects, it states that less than half of the campaigns were successful. The lay out of the data in Graph supports the theory that successful campaigns outweigh the failed and canceled campaigns. Louise should find comfort in knowing that most campaigns are, indeed, successful. 
- 2) Looking more carefully, it appears as if the spring and summer months are the most successful. May, in particular, has almost double the amount of successful campaigns with 111 recorded. It would therefore be recommended that Louise consider using a spring or summer month for her launch date. 

###Conclusions Drawn About Outcomes Based on Goals
The Outcomes Based on Goals data does not paint the most promising picture in Louis’ case. Based on Graph 1.2, the highest successful data point in the range is 76%. This is within the “Less Than 1000” goal bracket. This means that just over ¾ of the individuals who set a goal to raise less than $1000.00 were able to meet their goal. Those are pretty good odds. But Louis’ case is a bit different based on her goal bracket. 
Louis’ $12,000 would fall into the $10000 to $14999 range. 
According to the graph approximately 54% of Louise’ fundraising goal would likely be met.  This would leave Louise with the task of finding backers for the  46% remaining from her goal. So from $12,000, there would be an additional $5520.00 to collect ($12000 * 0.46 = $5520). 
Looking further at the data, arriving at success would more likely occur if Louis were to spend less than $5000.00 on her campaign. Does this mean she could possibly break her campaign up into two parts? Perhaps people are more inclined to support when there is a lower budget? 
###Limitations of this dataset? 
A limitation of this data set is the dates. This means the data collected does not reflect crowdfunding within the last five years. Five years could mark a large difference in crowdfunding activity. For instance, consider that these platforms are available online. The online world is continuously evolving and expanding. 

It is important to think of how many more users would be able to contribute based on new phone users, expanding lives online, aging population with disposable income, etc. There could also be reasons to decrease the pledges such as financial woes caused by the pandemic. 

###What are some other possible tables and/or graphs that we could create? 
For further analysis, it would also be insightful to see if gender plays a role in campaign funds. Women are currently receiving lots of newfound support in the world of performing arts. Does this indicate a potential sway for a female playwright as well?


