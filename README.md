# Kickstarter-Consultation
Analysis of what makes for a successful Kickstarter campaign


## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Data cleaning and Preperation](#data-cleaning-and-preperation)
- [EDA and Data Analysis](#eda-and-data-analysis)
- [Results and Findings](#results-and-findings)
- [Recommendations](#recommendations)

### Project Overview

|Analysis Steps|Tools|
|--------------|-----|
|Data Cleaning|Excel, Python|
|Data Preperation|Excel, Python|
|Data Analysis|SQL, Python, Tableau|
Findings and Recommendations|Tableau|


### Data Sources

The data is from early Kickstarter campaigns.

Attached above

### Data cleaning and Preperation

In the intial data preperation phase, I performed the following tasks:
1. Data loading and inspection
2. Handling null values
3. Data cleaning and formatting

I used pandas library in Python for intial data cleaning and identifying data types and null values. I uploaded the cleaned data into Tableau for further analysis. 

```python
import pandas as pd

kickstarter = pd.read_csv("./DAI_kickstarterscrape_dataset.csv", encoding='latin-1')

kickstarter.head()
kickstarter.dtypes
kickstarter.isnull().sum()
kickstarter.rename(columns={'project id':'project_id', 'funded percentage':'funded_percent', 'funded date':'fund_date', 'reward levels':'reward_levels'})
```

### EDA and Data Analysis

EDA involved in exploring Kickstarter campaigns

- What's the best length of time to run a campaign?
- What's the ideal pledge goal?
- What type of projects would be most successful at getting funded?
- Is there an ideal month/day/time to launch a campaign?

For this project I anlyzed what it takes to create a successful Kickstarter campaign. I identified what you should do and what you should avoid if you plan on starting a Kickstarter project to raise money. 

### Results and Findings

The most successful Kickstarter campaigns predominantly revolved around film and video projects and music projects. Documentaries and Short Films were the most successful amongst film and video projects. Rock and Indie Concerts were the most successful amongst music projects. Campaign duration also played a pivotal role in project success. The most successful Campaigns were around 30 days. Campaigns with a duration longer than one month were typically unsuccessful or cancelled. Project launch day should also be taken into consideration. Campaigns launched during the middle of the week had less success compared to campaigns launched Friday through Monday. Successful campaigns set an attainable goal around $5,000. Campaigns asking for more than $10,000 to $15,000 were typically unsuccessful. Successful campaigns also boasted substantial support from donor groups exceeding 100 backers.


### Recommendations

Set attainable campaign goal- less than $15,000

Keep campaign length around 1 month

Attain large community backing

Avoid launching in the middle of the week (Tuesday through Thursday)

Choose a project in Film/Video or Music areas

- Documentaries or Short Films
- Rock concerts




