# Cool title for the project

Perhaps "News polarisation: facts and myths"?

## Abstract

There are many news sources. How do we know which one to listen to?

We often hear that news are becoming increasingly political.
Not only that, they are also supposedly becoming more biased, or polarised, as well.

Can we measure such things with data analysis? Do such measures agree with our
intuitions?

Is this really the case? Can we see that in the data set?

## Research questions

- How can we measure politicization and polarisation of news sources?
- How politized and biased are different news sources?
- Are politicization and polarisation correlated with how popular a news source is?

## Proposed additional datasets

- Google Trends
- Wikidata information for news sources - home URLs, reader numbers
- Some social media message dataset (?)

## Methods

First, we will need to narrow down the Quotebank dataset so that running our
analysis doesn't take an excessively long time. The intention here is to let us
iterate over the implementation of our analysis as easily as possible. We can
remove all quotations that don't have a speaker identified. We can also split
the dataset by year, so that our analysis can be run just on a single year.

Then, we need to know which news sources we will try to understand. There's a
number of problems with the sources in the dataset - some of them appear to be
clones of each other, some appear to always redirect to other sources, and some
(judging on the URL) appear to have nothing to do with particular quotations.

To fix these problems, we will start by manually some news sources to initially
run the analysis on. We can write further stages of the pipeline based on these
sources while at the same time we will work on cleaning the news sources info.
As an additional benefit, starting with a smaller number of news sources will
let us iterate more quickly in the beginning.

As a measure of politicization of a news source, we propose to simply use the
percentage of quotations in a given news source that come from politicians.

To measure the bias of a news source, we propose to use affiliations of
politicians quoted in the source -- the more quotations come from politicians
affiliated with one side of the spectrum, the more biased a news source is.
However, some politicians are expected to appear more often than others in all
sources -- for instance, Trump. To offset this, we may need to use deviation
from the mean number of quotations rather than plain number of quotations for
each politican.

Measuring popularity of news sources depends on how many sources we have. If we
have sufficiently few sources, we could just manually find out their readership
numbers. If we consider every news source present in the cleaned data set, we
should automate this instead. We could potentially use Wikidata to identify news
sources based on their URLs and extract their reader numbers. Alternatively, we
could use a dataset of social media messages to extract how often a particular
news source is shared. It might also be interesting to have both these numbers --
perhaps non-biased sources have more readers overall, but it's the biased ones
that are most shared in social news?

Google Trends lets us check how often Google searches for a particular term are
performed. It does not offer precise search numbers, but it does let compare
different search terms. We could use it to compare select news sources and
validate our method of assessing how popular a news source is.

## Proposed timeline

We have the following separate tasks:

- News source cleanup
- Calculation of politicization/polarisation
- Calculation of popularity
- Calculation of correlation between politicization/polarisation and popularity
- Preparation of the data story (presentation techniques, preparing the story)

We can start working on other tasks without cleaning up the news sources, just
by working with a manual selection of news sources. Similarly, we can keep
investigating how to calculate correlation and present the data story (which
includes plotting the data in an interesting way) concurrently with other tasks.

The following is a tentative timeline until Christmas that includes a lot of
slack to account for, for instance, Homework 2:

- Week 1,2: calculate politicization/polarisation and popularity
- Week 3,4: calculate the correlation between politicization/polarisation and
  popularity
- Week 5,6: re-run the analysis on cleaned news sources, create the data story

## Organization

We will group tasks into four groups and for each group, we will pick a "leader".
The leader is the person responsible for ensuring tasks in the group
are progressing, but otherwise we will continue to meet, discuss and work together
on the tasks so that we evenly split the load. The groups are:

- News source cleanup & calculation of popularity
- Calculation of politicization/polarisation
- Calculation of correlation between politicization/polarisation and popularity
- Data story preparation

## Questions for the TAs
