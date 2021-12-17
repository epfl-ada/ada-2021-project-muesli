# Understanding news polarization

This repository contains the project of the group *Muesli* for the course [Applied Data Analysis](https://ada.epfl.ch) @ EPFL. 

## Abstract

Globally, politics has become increasingly polarized in recent years. Some argue that social networks are the main cause of this problem, but it is undeniable that the media also plays a key role in the political debate. 
Partisan media bias is defined as the situation in which a news source favors, criticizes, emphasizes or ignores certain political actors, policies, events or topics. 
In this project, we will analyse the frequency of reported quotes of politicians in several news sources to measure the politicization and polarization of the media. Secondly, we will dive deeper in the correlation between polarization and popularity to show whether the polarization of a news source influences its popularity. Lastly, we will classify the polarization of each news source by placing them in the political spectrum. 

## Data story

The data story can be found in this [website](https://giacomoorsi.github.io/usa-news-politicization/)

## Notebook

The folder `news_sources` contains information about the news sources that we analysed. 
The notebook, which contains both the data analysis and the plot generation, can be found [here](scripts/pipeline.ipynb)

## Group organization

We were able to follow the [timeline](project_proposal.md#timeline-and-organization) that we set in the milestone 2. In particular: 
 
- **Vittorio**: worked with Quotebank to reduce its size by removing unuseful information; revised the content of the data story
- **Stefan**: extracted useful information about speaker from WikiData; worked with Quotebank to filter the quotes of the selected news sources; documented the final notebook pipeline
- **Aleksander**: computed the statistics about politicization and polarization and prepared the plots; developed the analysis in the data story
- **Giacomo**: selected the news sources and researched current literature on media polarization; worked on repository documentation; developed the presentation of the data story on the website