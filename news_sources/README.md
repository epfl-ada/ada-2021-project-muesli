# News sources tables

The file `news-sources.csv` contains 20 news sources that we will use in our analysis. 

The file `all-news.csv` contains 27 news sources. I have removed those which are not very interesting (they don't have many visitors or they are not very politicized). 

### Table content

I have selected the news sources and added some features. 

|Column |Content|
|---|---|
|`name`|Name of the news source|
|`domain`|Main domain of the news source|
|`pew_democrats_survey`| Percentage of people that consider that news source left-biased
|`pew_republicans_survey`| Percentage of people that consider that news source left-biased
|`pew_difference`| Difference in abs between `pew_democrats_survey` and `pew_republicans_survey`
|`similarweb_total_visitors`| Number of visitor of the website (in millions) in the month of october 2021
|`similarweb_pages_per_visit`| Mean number of pages per visit on the website
|`similarweb_bounce_rate`| Bounce rate: percentage of one-page sessions over the total of sessions
|`twitter_followers`| Number of followers of their account on Twitter (millions)
|`notes`| Additional notes (optional)


### Data sources

- The data for the feature that start with `pew` come from a research on media bias with an [interesting data story](https://www.pewresearch.org/journalism/2020/01/24/u-s-media-polarization-and-the-2020-election-a-nation-divided/)
- Website data come for the website [Similarweb](similarweb.com)
- The number of followers on Twitter was picked manually 