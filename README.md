# Youtube_Analytics_Project

# Project Overview:

There is a lot of intention that goes into making a Youtube Channel, and the aim of this project was to look at data from top youtube channels to make recommendations to new Youtubers on how best to set up their channels. There are countless articles espousing advice on what tags are most popular, how often you should post videos (quality vs. quantity), and which countries produce the most popular content. We wanted to explore which of these really matter - which metrics actually relate to greater view counts and subscriber counts for channel, aiming our findings at the aspiring or up-and-coming Youtuber.

Using the 500 Youtube Channel names, we obtained the following information from the Youtube Data API:

- Channel Names 
- Channel Ids 
- Video Counts 
- View Counts 
- Subscriber Counts 
- Country of Origin 
- Genre Tags

# Hypotheses:

1. **Is there a relationship between genre tag and total view counts/subscriber counts/video counts?**
H0 : Count means are equal across genres, or  𝜇1=𝜇1=𝜇3 
H1 : Count means are not equal across genres - one


2. **Is there a relationship between country of origin and total view counts/subscriber counts/video counts?**
H0 : Count means are equal between countries, or  𝜇1=𝜇1=𝜇3 
H1 : Count means are not equal between countries

# Data Sources:

We used a data set of the top 500 Channels by Subscriber (as of 9/2019) from SocialBlade.com, and gathered information from the Youtube Data API on the fields described above. We used MySQL to store the data, and queried in Jupyter Notebook. We performed statistical analysis in Python using Pandas, using **statsmodels** and **scipy.stats**. All data visualizations were created using **Seaborn**.

# Statistical Analysis:

**One Way ANOVA on top 3 genre tags:**
(p<0.05) 

- Genre tag and View Count
- Genre tag and Subscriber Count
- Genre tag and Video Count

**Tukey Post Hoc Tests** on each revealed significant results for:

*View Count:*

- Entertainment - Lifestyle (Sociology)
- Lifestyle (Sociology) - Music

*Subscriber Count:*

- Lifestyle (Sociology) - Music
- Entertainment - Lifestyle (Sociology) 

*Video Count:*

- Entertainment - Lifestyle (Sociology)    
- Entertainment - Music


**One Way ANOVA on top 4 countries:**
(p<0.05) 

- Country of Origin and View Count
- Country of Origin and Subscriber Count
- Country of Origin and Video Count

**Tukey Post Hoc Tests** on each revealed significant results for:

*View Count:*

- India vs. Brazil

*Subscriber Count:*
- None

*Video Count:*

- Brazil vs. India
- India vs. N/A
- India vs. US


# Data Visualizations:

Genre tag Visualization:

Country Visualization:

# Recommendations and Insights:

Based on these findings, we suggest the following reccomendations to new Youtubers:

-In India, you  need to make a lot of video content to compete with top channels.

-If subscriber count is your main focus, consider creating a music channel rather than a lifestyle channel.

-If view count is your main focus, entertainment channels and music channels are more likely to bring in big viewership  than lifestyle channels ( good to consider for ad revenue!).

-Entertainment channels tend to produce more content, so if you want an entertainment channel to succeed consider quantity over quality..

# Study Limitations:

This study had a number of limitations. First, we had limited API calls for Youtube and were thus able to obtain less information from YouTube than we hoped for our original hypothesis. This inexperience meant we used our limited API resources ineffeciently; we would have collected much more robust datasets including video information if we had better understood the limitations from the start.

Additionally, we had a few limitations with our sample. One, we had large differences in sample sizes used in ANOVA which could have affected our results. We had less overall channels than we had originally planned on, thus yeilding a smaller overall sample size. Finally, we did not have time to remove all outliers from the data which likely affected our results.


