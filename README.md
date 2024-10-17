## Business Problem
___
If I had to start all over again with my career, I would have started building a social media audience from the beginning. In "Day Trading Attention," Gary Vaynerchuk explains that attention is one of the most valuable assets to modern businesses (this extends to personal brands, hence, my interest). His thesis is that one of the highest Return on Investment (ROI) ways to capture that attention is to use organic social media and to make content that people want to consume. 

But, as a late comer to social media, it is kind of unclear what the average person wants to watch. By extension, it may not be clear to a business what kind of content they should be creating and how to position that content if they haven't created any up to the present day.

Therefore, we can set up a couple of questions:
1. How are creators in our niche currently getting their content in front of the right people organically? More specifically, what hashtags are they using to help communicate their target audience to the platform's algorithm?
2. Who are the current top performers in our niche in terms of views and engagement? 
3. Assuming we are starting from scratch, can we identify some creators in our niche that have low follower counts but have high views and engagement? This could inform a strategy for scaling quickly.

In this project, we will focus on TikTok due to a couple of features of the platform:
- Interest based algorithm, which allows new accounts with low followers to get a relatively high view rate IF they have content that aligns with the target audience's interests.
- Industry leading short form video format.
### Data Source
___
Data has been scraped from a search completed on TikTok's website. A semi-manual technique that is compatible with TikTok's Terms & Conditions has been used.

Briefly, this technique is as follows:
1. Sign in to TikTok's website through a desktop browser.
2. Complete a search term related to the niche of the business that we are strategizing for. In this case, we will use "Organic Marketing" as the search term. 
3. Open developer tools in the browser. Refresh the page and open the Network tab. Search "full/" 
4. Scroll through the search results to collect more responses for video search results.
5. Save the JSON files that have been collected as a HAR file. 

This HAR file will be used as the initial raw data source.

The search term used in this case is "Content Creator Tips." This is because of my personal interest and immediate value of the data to these interests. A data driven approach could provide a different perspective than most creators in this space, currently.
### Methods and Tech Used
___
- Web development tools are used to gather data, as previously mentioned.
- A jupyter notebook and python have been used for data cleaning, aggregation, manipulation, and visualization
### Results
___
*1. How are creators in our niche currently getting their content in front of the right people organically? More specifically, what hashtags are they using to help communicate their target audience to the platform's algorithm?*
![alt text](assets/TotalViewCountPieChart.png)

The 'Top Hashtags by Total View Count' pie chart reveals the hashtags associated with the most views for the search query 'Content Creator Tips.' Unsurprisingly, #contentcreatortips is the top result, probably due to how TikTok calculates their Search Engine Optimization (SEO). But, it is worth noting that the rest of the 24 hashtags offer some other ideas of how one might use hashtags to get in front of an audience interested in content creator tips. **Some other tangential customer segments may also be identified. Such as UGC creators, people interested in social media marketing, or people interested in TikTok news.**

![alt text](assets/AvgEngagementPieChart.png)

An interesting insight can be gained from the second pie chart, 'Top Hashtags by Average Engagement Rate.' The posts with the highest engagement are associated with more actionable and specific hashtags. Accounts can get a lot more interaction with the audience by talking about photography tips, and tools to create content such as the Creator Search Insights tool and the Greenscreen effect used in the content creation part of the app. **New accounts could use this information to form a stronger relationship with the audience in the early stages of entering a niche.**

*2. Who are the current top performers in our niche in terms of views and engagement?*
![alt text](assets/AllTop10Accounts.png)
Thes Bar Charts show the Top 10 accounts in terms views and engagement metrics. From the charts, **we can identify laurennrwebb, laurenwolfe, rixirising, milajaye, tipsforcreators, lo_silver, and amymarietta as top-performing accounts**. These accounts appear on multiple charts, indicating consistent performance across different metrics and reducing the likelihood that their success is due to outliers.

The 'Top 10 Accounts by Comments' bar chart does present an interesting observation. Milajaye is by far an outlier for the amount of comments that she generates. More than 5x second place. Further investigation is needed to understand why this account is performing so well. Potentially, it could be here Call to Action (CTA), her subject matter (iPhone photography generates more engagement, as we discussed), or maybe the audience cohort that she appeals to.

*3. Assuming we are starting from scratch, can we identify some creators in our niche that have low follower counts but have high views and engagement? This could inform a strategy for scaling quickly.*
![alt text](assets/ScatterPlotViewsVsFollowers.png)
The scatter plot uses a logarithmic scale to chart view count vs. follower count. The user can highlight the dots in the plot generated in the jupyter notebook to identify the account and it's X and Y values. 
**For a new account, a tool like this can be used to identify accounts that have performed well with a relatively low follower count.**

![alt text](assets/LassoOnScatterPlot.png)
For example, the accounts contained in the circle above have under 10k followers, but over 200k views on the video that appears in this search query. Investigating this video, and the account may indicate variables that could be used to mimic this virality.

### Limitations 
___
- The search results can be influenced by the user account used to complete the search during the data gathering phase. 
	- Previous engagement with specific hashtags and accounts may alter the results that are returned.
	- The location of the device used to complete the search alters results. 
- On the desktop website, results can not be filtered by date. Therefore, videos that benefited from trends and first mover advantage can skew the applicability of insights gained.
- The results of this search are just a snapshot. For time series analysis, one would have to create multiple HAR files and store the data for an extended period of time. 