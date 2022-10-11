# Professionalism & Responsibility 
#### Homework 1

This repository contains the code used to analyze the access data of dinosaur articles on Wikipedia from July 2015 through September 2022. This analysis results in time series plots that look at the views over time of different subsets of the articles. Specifically, the code will produce plots for the following subsets of articles: Maximum and Minimum Average Views, Top 10 Peak Page Views, and Fewest Months of Data. 

The raw dataset contains the names and urls for a subset of Wikipedia articles related to dinosaurs. The dataset can be found in the file dinosaur_subset.xlsx located within the repo. It's source location is here: https://docs.google.com/spreadsheets/d/1zfBNKsuWOFVFTOGK8qnTr2DmHkYK4mAACBKk1sHLt_k/edit#gid=1345871712. 

The Wikimedia REST API is used to collect access data for the articles within the dataset. The licence information for the REST API can be found here: https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end and the terms and conditions for use of this API are located here: https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions.  

The REST API was called using the function defined in the notebook, wp_article_views_example.ipynb, located in this repo. This code example was developed by Dr. David W. McDonald for use in DATA 512, a course in the UW MS Data Science degree program. This code is provided under the Creative Commons CC-BY license (https://creativecommons.org/licenses/by/4.0/). 

The REST API is used to collect access data for the dinosaur articles. Three files are produced using this API, which are described below: \
dino_monthly_mobile_201507-202210.json - containing the data for articles that were accessed from a mobile device between July 2015 and September 2022. \
dino_monthly_desktop_201507-202210.json - containing the data for articles that were accessed from a desktop between July 2015 and September 2022. \
dino_monthly_desktop_201507-202210.json - containing the data for articles that were accessed from either a desktop or a mobile device between July 2015 and September 2022. 

These files have the following variables: 
Name | Definition 
--- | --- 
project | domain of the Wikimedia project
article | title of the article in the project
granularity | time unit of the views data
timestamp | year/month of access data
access | access method
agent | agent type (user, automated, or spider)
views | total views during month of timestamp 

The analysis is conducted on the mobile and desktop datasets and produces the following three plots: \
Max_Min_Article_Views.png - timeseries plot of the maximum and minimum views for articles by access type \
Top_10_Max_Page_Views.png - timeseries plot of the articles with the top ten peak views for each access type \
Fewest_Months_Of_Data.png - timeseries plot of the articles with the ten fewest months of data for each access type 



