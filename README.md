## Introduction
This project investigates how universities have communicated about diversity, equity, and inclusion (DEI) over time on X (formerly, Twitter). Using over 8 million tweets from five university accounts spanning 2010–2022, I applied natural language processing techniques to classify tweets as DEI-related or not. 

## Exploratory Data Analysis
I performed exploratory analysis to understand the linguistic and thematic differences between DEI and non-DEI tweets, and to uncover general patterns within the dataset.

### Histogram
Tweet volume from US universities (2010-2022) shows strong initial growth, peaking around 2014-2015, followed by a consistent decline in subsequent years.

![Histogram of 8M Tweets over 2010 to 2022](/Visualizations/Histograms/Histogram_Whole%20Dataset.png)

### TF-IDF Analysis
To better understand the language patterns surrounding diversity, equity, and inclusion (DEI) in university discourse, I applied Term Frequency–Inverse Document Frequency (TF-IDF) analysis across various slices of the dataset. TF-IDF helps highlight words that are particularly significant in a subset of texts relative to the broader corpus, making it a valuable tool for surfacing context-specific DEI terms.

This analysis was conducted at multiple levels:
- across the full dataset of tweets,
- within individual university accounts,
- across time brackets (early years, mid-period, and recent years),
- by university rank (top, middle, and bottom), and
- around key social movements such as #MeToo, Black Lives Matter, and Stop Asian Hate.

#### Top DEI Words

**Across Entire Dataset**

This analysis identifies the top DEI-related terms across the full corpus of university tweets. Words such as "woman", "diversity", "justice" appear with higher scores.


![Top DEI Words across Entire Dataset](/Visualizations/TF-IDF%20Analysis/top_dei_keywords_by_tf_idf_score_whole_dataset.png)


**By Events**

The top DEI words found for the event, Black Lives Matter, is shown below. TF-IDF scores before, during, and after the BLM protests show a clear shift in language from general terms to more urgent and justice-oriented vocabulary like "police brutality", "systemic racism", "racial injustice" etc. This highlights how a major event shifted the discourse.

![Top DEI Words for Black Lives Matter](/Visualizations/TF-IDF%20Analysis/blm_progression.png)


**By Year Brackets**

DEI language has evolved notably over time—earlier years featured generic terms like diversity, fair, women, while more recent years emphasized black, access, and justice

![Top DEI Words by Year Brackets](/Visualizations/TF-IDF%20Analysis/top_dei_keywords_by_year_brackets.png)

### Hashtag Analysis

DEI-related hashtag usage is dominated by #blackhistorymonth (over 7,000 uses; 22.8% share) and #womenshistorymonth (over 5,000 uses; 16.5%). 

![Top DEI Hashtags Across the Entire Dataset](/Visualizations/Hashtag%20Analysis/top_dei_hashtags_allschools.png)

### Tweet Classification
 
To enable DEI-related tweet classification, I **manually** curated a labeled dataset with approximately over 2000 tweets, ensuring balanced representation from school accounts, rankings, regions, and periods. Then, I used this to finetune a bertweet model and used it to classify the 8M tweets as DEI or Non-DEI.

**Some key insights from the classification**

Over time, the DEI discourse reaches its peak at 2020/2021, suggesting the surge of DEI conversations during that time due the events like the Black Lives Matter movement, Covid19 Pandemic, and the US Presidential Election.

![Predicted DEI Trend Over the Years](/Visualizations/Trend%20over%20the%20Years/Whole_Dataset_8Mtweets.png)

