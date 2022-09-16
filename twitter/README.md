# Data

## Description

The corpus used in this Task is based on a large-size multilingual collection of tweets sampled from the Twitter public streaming API using keywords like [“COVID19”, “CoronavirusPandemic”, “COVID-19”, “2019nCoV”, “CoronaOutbreak”, “coronavirus”, “WuhanVirus"], described in:

Banda, J.M.; Tekumalla, R.; Wang, G.; Yu, J.; Liu, T.; Ding, Y.; Artemova, E.; Tutubalina, E.; Chowell, G. A Large-Scale COVID-19 Twitter Chatter Dataset for Open Scientific Research—An International Collaboration. Epidemiologia 2021, 2, 315-324. https://doi.org/10.3390/epidemiologia2030024

The source data of this collection, together with documentation on how to process the data, can be found on

https://github.com/thepanacealab/covid19_twitter.

We use the clean version of this dataset that was already filtered for retweets. The collection of tweets is language tagged since July 27 2020. We further filter the data from July 27 2020 through October 26 2020 and produce two monolingual tweet collections for English and Spanish. 

Namely, in order to restrict the sample to content from the US context, we filter for tweets which have a "Place" metadata with country_code="us" or (if "Place" is None) with a "User" location specified as one of the US States. For each day, we filter up to reaching a sampling cap of 0.1 and 0.5 of the original tweet collections, for English and Spanish respectively.

The overall size of the tweet collections are about X and 46k, for English and Spanish, respectively, with an average of X and 503 tweets by day. 

## Downloading Tweet Content

Due to Twitter's Terms of Service, we are only able to distribute the numeric tweet ids. We release in:

twitter\tweets_ids_2020-07-27_2020-10-26_en.tsv
twitter\tweets_ids_2020-07-27_2020-10-26_es.tsv

the time ordered lists of English and Spanish tweet ids.

Here we give brief instructions on how to populate the full tweet data from the list of ids. To do this we will use the Python command line tool [Twarc](https://github.com/DocNow/twarc). The following steps assume you have Twarc installed as well as a [Twitter Developer account](https://developer.twitter.com/en/apply-for-access). To install Twarc, please run

```
pip3 install twarc
```

Next, you must configure Twarc with your [Twitter API tokens](https://developer.twitter.com/en/apply-for-access). 

```
twarc configure
```

Next, download the data from GitHub:

```
git clone https://github.com/zavavan/CASE2022_Task2.git
cd CASE2022_Task2\twitter
```

### Using twarc from the command line

This command will produce a file where each line is a separate json file for each tweet ids. Note that only tweets which are publicly available at the time of your pull will be downloaded. Thus, our numbers might not match the numbers you see. 

```
twarc hydrate tweets_ids_2020-07-27_2020-10-26_es.txt > tweets_ids_2020-07-27_2020-10-26_es.jsonl
```

### Other options 

Besides twarc, there are many other tools available for downloading Twitter data, such as [TwitterMySQL](https://github.com/dlatk/TwitterMySQL) and [hydrator](https://github.com/DocNow/hydrator).


## Partially Hydrated Tweet Collections

In order to facilitate the running of the participant systems on the data, we provide also files with daily collections of partially hydrated tweets. We expose basic metadata fields which might be used to geocode the tweets. For each day <date> and language <lang>, we provide a jsonl file named:

hydrated_tweets_<date>_<lang>.jsonl

where each line encodes a tweet in json format with the following fields:

 ['created_at','id','full_text','geo','coordinates','place','lang',"user"]
 
The data will be distributed via a private folder to Task 2 participant systems only. Please contact ali.hurriyetoglu@gmail.com or vanzavavan@gmail.com for details.
