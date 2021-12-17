# Understanding news polarization

In this document, we will explain our idea for an analysis of the Quotebank dataset. In particular, we will address the results that we aim to obtain and the methodologies that we will use. 

## Abstract

Globally, politics has become increasingly polarized in recent years. Some argue that social networks are the main cause of this problem, but it is undeniable that the media also plays a key role in the political debate. 
Partisan media bias is defined as the situation in which a news source favors, criticizes, emphasizes or ignores certain political actors, policies, events or topics [1]. 
In this project, we will analyse the frequency of reported quotes of politicians in several news sources to measure the politicization and polarization of the media. Secondly, we will dive deeper in the correlation between polarization and popularity to show whether the polarization of a news source influences its popularity. Lastly, we will classify the polarization of each news source by placing them in the political spectrum. 


## Research questions

- How can we measure the politicization and polarization of news sources by analysing the quotes they publish?
- How politicized and biased are different news sources? What’s their position in the political spectrum?
- Are politicization and polarization correlated with how popular a news source is?


## Proposed additional datasets

- WikiData, to extract information about the news source (home URLs, reader numbers, country) and the speaker (if he/she is a politician, political party)
- Google Trends, to analyze the notoriety of a news source
- Twitter APIs and/or Social Media Datasets to analyze the popularity of a news source


## Methods
In this section, we will address the methodology that we will use to process the dataset and carry out our analysis. 

### Quotebank dataset cleaning

All the quotations without an identified speaker will be removed and the dataset will be split by year so that we can easily run our computation on a partial dataset. 

Some quotations have a list of speakers with an associated probability. We will keep only the quotations assigned to a speaker with a probability greater than a predefined threshold.

Our data story will address the polarization of the most well-known news sources in the USA which deal with US politics. In order to realize an interesting and engaging data story, we have decided to do our analysis only on a small number of news sources (around 20). Therefore, we will manually select such news sources based on their popularity in the USA.  All the other news sources will be removed. 


### Computing politicization and polarization

As a measure of the politicization of a news source, we will calculate the percentage of quotations made by people affiliated with a political party. To do this, we will first match each speaker with their political party using Wikidata. Secondly, we will compute the number of quotes reported for each side of the political spectrum. However, some politicians are expected to appear more often than others in all sources. For instance, governors or the President will be likely to appear often in all news sources, regardless of their level of polarization. Therefore, we will use the deviation from the mean in the number of quotes for each party to classify the polarisation of a news source.

### Understanding correlations between politicization, polarization and popularity

Measuring popularity is a challenging task because it can be done from both a quantitative and qualitative point of view and it’s an open question in sociological research [2]. Something popular is often associated with something which is liked by a large part of the population. Nevertheless, popularity on social media can be associated with opposite sentiments like disgust and indignation. Therefore, we will define popularity with a set of quantitative parameters. Some of them are publicly made available by the news sources (e.g. paying subscribers), some are provided by internet audit companies (e.g. monthly visitors) and some can be derived using online tools (e.g. number of Google Searches using Google Trends). We will compute the popularity of a news source on social media by using Twitter APIs or a Social Media dataset. 

### Presenting our results

> Science is not finished until it is communicated (Mark Walport)

We strongly believe that this research will be meaningful if we will be able to communicate our findings effectively. Therefore, we will construct an engaging data story that will explain how we reached our conclusions and contains information on the political events that took place during the period analysed.


## Timeline and organization

We will need to perform the following tasks:

1. Quotations filtering 
2. Computing the politicization/polarization of news sources
3. Computing the popularity of news sources
4. Computing the correlation between politicization/polarization and popularity
5. Preparing the data story (presentation techniques, preparing the story, political events)


Tasks (1) and (3) can be performed at the same time. Once finished, we will be able to work on task (2) and (4). As described above, the data story will play an important role in our research project. As a consequence, we will start working on its draft in the early stages of the project.  

We will follow this timeline:


- Week 1, 2: tasks (1) and (3)
- Week 3, 4: tasks (2) and (4) and (5)
- Week 5, 6: tasks (4) and (5)

Each of the listed tasks will require a lot of effort. Therefore, we will pick a *leader* for each of them who will ensure that his tasks are progressing. We will meet regularly to be able to evenly split the workload. 


## Organization

We will group tasks into four groups and for each group, we will pick a "leader". The leader is the person responsible for ensuring tasks in the group are progressing, but otherwise we will continue to meet, discuss and work together on the tasks so that we evenly split the load. The groups are:


- News source cleanup & calculation of popularity
- Calculation of politicization/polarization
- Calculation of correlation between politicization/polarization and popularity
- Data story preparation

## Questions for TAs

We would be grateful for a suggestion of a dataset that we could use to analyse the popularity of a news source on social media.

## References

[1]: Shultziner D, Stukalin Y. Distorting the News? The Mechanisms of Partisan Media Bias and Its Effects on News Production. Political Behavior. 2021;43(1):201–222. doi:10.1007/s11109-019-09551-y.

[2]: Cillessen, Antonius HN, and Peter EL Marks. "Conceptualizing and measuring popularity." Popularity in the peer system (2011): 25-56.
