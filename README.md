# Kickstarting with Excel

## Overview of Project
Our client wishes to perform a crowdfunding campaign for a play. To understand the likelihood of success and to define the characteristics of successful campaigns, we have been retained to examine the results of previous campaigns.

### Purpose
We hope to optimize our chances of success by examining previous campaigns.

## Analysis and Challenges
We were provided with insights into 4,113 crowdfunding campaigns. The campaigns were from multiple countries and covered many industries. Of the 4,113 campaigns, 1393 were for theater, and only 314 were for plays in Great Britain.

To provide greater clarity on the outcomes of the campaigns we examined the date(s) of the campaign, and the amount pledged relative to the campaign goal. Using these, we categorized each campaign as successful, failed, live, or canceled.
We established counts for all the categories using the formula =COUNTIFS(Kickstarter!$F:$F,"successful", Kickstarter!$R:$R,"=plays",Kickstarter!$D:$D,"<1000")

In addition, we standardized the dates using the following formula: =(((J2/60)/60)/24)+DATE(1970,1,1)

### Analysis of Outcomes Based on Launch Date
Using our standardized dates and new categorizations, we created a pivot table and charted out the results. Discussion of these results can be found in the results section below.
![image](https://user-images.githubusercontent.com/94585985/143817943-2fe3b283-3040-4649-a9c2-266069587e98.png)
![image](https://user-images.githubusercontent.com/94585985/143818188-129fb82c-493b-4a0e-a7b1-1fff14ad5020.png)


### Analysis of Outcomes Based on Goals

We bucketed campaigns for plays by Goals, and set up counts for successful, failed, and canceled projects.  The corresponding tables and chart can be seen below, with discussion of results in the results section.

<img width="531" alt="Screen Shot 2021-11-28 at 10 49 36 PM" src="https://user-images.githubusercontent.com/94585985/143821245-80e21ebf-2902-429d-83c5-66b986cfed08.png">

<img width="449" alt="Screen Shot 2021-11-28 at 10 50 39 PM" src="https://user-images.githubusercontent.com/94585985/143821361-91f34fd4-cb1b-4db8-8d9d-4191da9e3518.png">

### Challenges and Difficulties Encountered
The most challenging part of this project was the manual categorization of the goals. Each bucket needed to be manually created and typed into each cell for the first column that used the categorization. The difficulty of this process was even more apparent when it turned out the buckets were too narrowly defined, with few projects in the larger goal categories.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
The most common month to launch campaigns is May and the months that follow. The least common month to launch a campaign is December. This is most likely explained by the 67% success rate for campaigns that launch in May, which compares favorably to the 49% success rate for campaigns launched in the busy holiday season in December.

- What can you conclude about the Outcomes based on Goals?
Broadly speaking, the larger the goal, the less likely the project will be to succeed.  The results are somewhat obscured because of the categorizations used to bucket the goals.  Had all goals over 15000 been collapsed into a single category, the results would have been more apparent. Given that there were so few observations in the higher categories, there is a lot of noise.

- What are some limitations of this dataset?
The single biggest limitation of the dataset are the underlying drivers of the results.  We don't know who they contacted, how they contacted them, what they offered or pitched as part of the campaign etc.

- What are some other possible tables and/or graphs that we could create?
I think it would be interesting to look at length of the campaigns, categorize the markets for the campaigns below the country level into market type, and possibly look at the impact of economic or demographic information. 
